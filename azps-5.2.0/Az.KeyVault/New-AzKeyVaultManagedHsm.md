---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337015"
---
# New-AzKeyVaultManagedHsm

## Sinossi
Crea un HSM gestito.

## SINTASSI

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzKeyVaultManagedHsm** crea un HSM gestito nel gruppo di risorse specificato. Per aggiungere, rimuovere o elencare le chiavi nell'HSM gestito, l'utente deve concedere le autorizzazioni aggiungendo l'ID utente all'amministratore.

## ESEMPI

### Esempio 1: creare un HSM gestito StandardB1
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Questo comando crea un HSM gestito denominato myhsm nella posizione eastus2euap. Il comando aggiunge l'HSM gestito al gruppo di risorse denominato myrg1. Poiché il comando non specifica un valore per il parametro *SKU* , crea un Standard_B1 HSM gestito.

### Esempio 2: creare un HSM gestito CustomB32
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

Questo comando crea un HSM gestito, proprio come nell'esempio precedente. Tuttavia, specifica un valore di CustomB32 per il parametro *SKU* per creare un HSM gestito CustomB32.

## PARAMETRI

### -Amministratore
ID oggetto amministratore iniziale per questo pool di HSM gestito.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AsJob
Esegui cmdlet in background

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Specifica l'area di Azure in cui creare il Vault chiave.
Usa il comando Get-AzResourceProvider con il parametro ProviderNamespace per visualizzare le tue scelte.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica un nome dell'HSM gestito da creare.
Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.
Il nome deve iniziare e terminare con una lettera o una cifra.
Il nome deve essere universalmente univoco.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica l'USK dell'istanza di HSM gestita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Tabella hash che rappresenta i tag delle risorse.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### System. String []

### System. Collections. Hashtable

## OUTPUT

### Microsoft. Azure. Commands. Vault. Models. PSManagedHsm

## Note

## COLLEGAMENTI CORRELATI

[Get-AzKeyVaultManagedHsm](./Get-AzKeyVaultManagedHsm.md)

[Remove-AzKeyVaultManagedHsm](./Remove-AzKeyVaultManagedHsm.md)

[Update-AzKeyVaultManagedHsm](./Update-AzKeyVaultManagedHsm.md)