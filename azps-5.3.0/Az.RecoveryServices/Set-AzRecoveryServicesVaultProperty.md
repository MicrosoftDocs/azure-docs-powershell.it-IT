---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475784"
---
# <span data-ttu-id="83afc-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="83afc-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="83afc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83afc-102">SYNOPSIS</span></span>
<span data-ttu-id="83afc-103">Aggiorna le proprietà di un Vault.</span><span class="sxs-lookup"><span data-stu-id="83afc-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="83afc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83afc-104">SYNTAX</span></span>

### <span data-ttu-id="83afc-105">AzureRSVaultSoftDelteParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83afc-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83afc-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="83afc-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83afc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83afc-107">DESCRIPTION</span></span>
<span data-ttu-id="83afc-108">Il cmdlet **set-AzRecoveryServicesVaultProperty** aggiorna le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="83afc-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="83afc-109">Questo cmdlet può essere usato per abilitare/disabilitare l'eliminazione morbida o impostare la crittografia CMK per un Vault con due diversi set di parametri.</span><span class="sxs-lookup"><span data-stu-id="83afc-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="83afc-110">La proprietà **SoftDeleteFeatureState** di un Vault può essere disabilitata solo se non sono presenti contenitori registrati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="83afc-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="83afc-111">InfrastructurEncryption può essere impostato solo la prima volta che un utente aggiorna il Vault CMK.</span><span class="sxs-lookup"><span data-stu-id="83afc-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="83afc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83afc-112">EXAMPLES</span></span>

### <span data-ttu-id="83afc-113">Esempio 1: aggiornare SoftDeleteFeatureState di un Vault</span><span class="sxs-lookup"><span data-stu-id="83afc-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="83afc-114">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="83afc-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="83afc-115">Il secondo comando Aggiorna la proprietà SoftDeleteFeatureState della volta in stato "Enabled".</span><span class="sxs-lookup"><span data-stu-id="83afc-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="83afc-116">Esempio 2: aggiornamento della crittografia CMK di un Vault</span><span class="sxs-lookup"><span data-stu-id="83afc-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="83afc-117">Il primo cmdlet ottiene il RSVault per aggiornare le proprietà di crittografia.</span><span class="sxs-lookup"><span data-stu-id="83afc-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="83afc-118">Secondo cmdlet ottiene l'archiviazione delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="83afc-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="83afc-119">Il terzo cmdlet ottiene la chiave dal Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="83afc-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="83afc-120">Il quarto cmdlet aggiorna la chiave di crittografia gestita dal cliente all'interno di RSVault.</span><span class="sxs-lookup"><span data-stu-id="83afc-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="83afc-121">USA-InfrastructureEncryption param per abilitare la crittografia dell'infrastruttura per l'aggiornamento per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="83afc-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="83afc-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83afc-122">PARAMETERS</span></span>

### <span data-ttu-id="83afc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83afc-123">-DefaultProfile</span></span>
<span data-ttu-id="83afc-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83afc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83afc-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="83afc-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="83afc-126">SoftDeleteFeatureState del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="83afc-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afc-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="83afc-127">-EncryptionKeyId</span></span>
<span data-ttu-id="83afc-128">KeyId della chiave di crittografia da usare per CMK.</span><span class="sxs-lookup"><span data-stu-id="83afc-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afc-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83afc-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="83afc-130">ID sottoscrizione del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="83afc-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afc-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="83afc-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="83afc-132">Abilita la crittografia dell'infrastruttura in questo Vault.</span><span class="sxs-lookup"><span data-stu-id="83afc-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="83afc-133">La crittografia dell'infrastruttura deve essere abilitata durante la configurazione della crittografia.</span><span class="sxs-lookup"><span data-stu-id="83afc-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83afc-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="83afc-134">-VaultId</span></span>
<span data-ttu-id="83afc-135">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="83afc-135">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83afc-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83afc-136">-Confirm</span></span>
<span data-ttu-id="83afc-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83afc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83afc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83afc-138">-WhatIf</span></span>
<span data-ttu-id="83afc-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83afc-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="83afc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83afc-140">CommonParameters</span></span>
<span data-ttu-id="83afc-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83afc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83afc-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83afc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83afc-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83afc-143">INPUTS</span></span>

### <span data-ttu-id="83afc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="83afc-144">System.String</span></span>

### <span data-ttu-id="83afc-145">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="83afc-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="83afc-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83afc-146">OUTPUTS</span></span>

### <span data-ttu-id="83afc-147">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="83afc-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="83afc-148">Note</span><span class="sxs-lookup"><span data-stu-id="83afc-148">NOTES</span></span>

## <span data-ttu-id="83afc-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83afc-149">RELATED LINKS</span></span>

[<span data-ttu-id="83afc-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="83afc-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="83afc-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="83afc-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
