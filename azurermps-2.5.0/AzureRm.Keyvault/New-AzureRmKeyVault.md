---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: b40a37729d52cfe3b1dba691fd11724fcd0b03fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866107"
---
# New-AzureRmKeyVault

## Sinossi
Crea un Vault chiave.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmKeyVault** crea un Vault Key nel gruppo di risorse specificato. Questo cmdlet concede anche le autorizzazioni per l'utente attualmente connesso per aggiungere, rimuovere o elencare chiavi e segreti nel caveau della chiave.

Nota: se viene visualizzato l'errore **l'abbonamento non è registrato per l'uso dello spazio dei nomi "Microsoft. Key Vault"** quando si tenta di creare il nuovo Vault chiave, eseguire **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. Key Vault"** e quindi eseguire di nuovo il comando **New-AzureRmKeyVault** . Per altre informazioni, vedere Register-AzureRmResourceProvider.

## ESEMPI

### Esempio 1: creare un Vault chiave standard
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

Questo comando crea un Vault chiave denominato Contoso03Vault, nell'area di Azure est US. Il comando aggiunge il Vault chiave al gruppo di risorse denominato Group14. Poiché il comando non specifica un valore per il parametro *SKU* , crea un Vault chiave standard.

### Esempio 2: creare un Vault Key Premium
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

Questo comando crea un Vault chiave, proprio come nell'esempio precedente. Tuttavia, specifica un valore Premium per il parametro *SKU* per creare un Vault Key Premium.

## PARAMETRI

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableSoftDelete
Specifica che la funzionalità di eliminazione morbida è abilitata per il Vault chiave. Quando è abilitata l'eliminazione morbida, per un periodo di tolleranza, è possibile recuperare il Vault chiave e il relativo contenuto dopo l'eliminazione.

Per altre informazioni su questa funzionalità, vedere [Panoramica dell'eliminazione di Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete). Per istruzioni su come fare, Vedi [come usare Key Vault soft-delete con PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Posizione
Specifica l'area di Azure in cui creare il Vault chiave. Usare il comando [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) per visualizzare le opzioni desiderate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Specifica l'USK dell'istanza Key Vault. Per informazioni sulle caratteristiche disponibili per ogni Usk, vedere il sito Web relativo ai prezzi di Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore in forma di tabella hash. Per esempio:

@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VAULTNAME
Specifica il nome del Vault della chiave da creare. Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini. Il nome deve iniziare e terminare con una lettera o una cifra. Il nome deve essere universalmente univoco.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. Azure. Commands. Vault. Models. PSVault

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
