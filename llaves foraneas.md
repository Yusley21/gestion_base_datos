# gestion_base_datos
proyecto maternidad

---------------llaves foraneas
alter table ADMINISTRACION
   add constraint FK_ADMINIST_RELATIONS_MADRE foreign key (ID_MADRE)
      references MADRE (ID_MADRE)
      on delete restrict on update restrict;

alter table BEBE
   add constraint FK_BEBE_RELATIONS_MADRE foreign key (ID_MADRE)
      references MADRE (ID_MADRE)
      on delete restrict on update restrict;

alter table BEBE
   add constraint FK_BEBE_RELATIONS_PERSONAL foreign key (ID_PERSONAL)
      references PERSONAL_MATERNIDAD (ID_PERSONAL)
      on delete restrict on update restrict;

alter table INCUBADORA
   add constraint FK_INCUBADO_RELATIONS_BEBE foreign key (ID_BEBE)
      references BEBE (ID_BEBE)
      on delete restrict on update restrict;

alter table INCUBADORA
   add constraint FK_INCUBADO_RELATIONS_PERSONAL foreign key (ID_PERSONAL)
      references PERSONAL_MATERNIDAD (ID_PERSONAL)
      on delete restrict on update restrict;

alter table QUIROFANO
   add constraint FK_QUIROFAN_RELATIONS_BEBE foreign key (ID_BEBE)
      references BEBE (ID_BEBE)
      on delete restrict on update restrict;

alter table QUIROFANO
   add constraint FK_QUIROFAN_RELATIONS_MANTENIM foreign key (ID_MANTENIMIENTO)
      references MANTENIMIENTO (ID_MANTENIMIENTO)
      on delete restrict on update restrict;

alter table QUIROFANO
   add constraint FK_QUIROFAN_RELATIONS_PERSONAL foreign key (ID_PERSONAL)
      references PERSONAL_MATERNIDAD (ID_PERSONAL)
      on delete restrict on update restrict;

alter table QUIROFANO
   add constraint FK_QUIROFAN_RELATIONS_MADRE foreign key (ID_MADRE)
      references MADRE (ID_MADRE)
      on delete restrict on update restrict;

alter table SALA_PARTO
   add constraint FK_SALA_PAR_RELATIONS_BEBE foreign key (ID_BEBE)
      references BEBE (ID_BEBE)
      on delete restrict on update restrict;

alter table SALA_PARTO
   add constraint FK_SALA_PAR_RELATIONS_MANTENIM foreign key (ID_MANTENIMIENTO)
      references MANTENIMIENTO (ID_MANTENIMIENTO)
      on delete restrict on update restrict;

alter table SALA_PARTO
   add constraint FK_SALA_PAR_RELATIONS_PERSONAL foreign key (ID_PERSONAL)
      references PERSONAL_MATERNIDAD (ID_PERSONAL)
      on delete restrict on update restrict;

alter table SALA_PARTO
   add constraint FK_SALA_PAR_RELATIONS_MADRE foreign key (ID_MADRE)
      references MADRE (ID_MADRE)
      on delete restrict on update restrict;
