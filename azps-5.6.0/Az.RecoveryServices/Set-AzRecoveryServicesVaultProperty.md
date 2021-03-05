---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997385"
---
# <span data-ttu-id="763c5-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="763c5-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="763c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="763c5-102">SYNOPSIS</span></span>
<span data-ttu-id="763c5-103">Aggiorna le proprietà di un Vault.</span><span class="sxs-lookup"><span data-stu-id="763c5-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="763c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="763c5-104">SYNTAX</span></span>

### <span data-ttu-id="763c5-105">AzureRSVaultSoftDelteParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="763c5-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="763c5-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="763c5-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="763c5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="763c5-107">DESCRIPTION</span></span>
<span data-ttu-id="763c5-108">Il cmdlet **Set-AzRecoveryServicesVaultProperty** aggiorna le proprietà di un vault dei servizi di recupero.</span><span class="sxs-lookup"><span data-stu-id="763c5-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="763c5-109">Questo cmdlet può essere usato per abilitare/disabilitare l'eliminazione temporaneamente o impostare la crittografia CMK per un vault con due set di parametri diversi.</span><span class="sxs-lookup"><span data-stu-id="763c5-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="763c5-110">**La proprietà SoftDeleteFeatureState** di un vault può essere disabilitata solo se nel vault non sono presenti contenitori registrati.</span><span class="sxs-lookup"><span data-stu-id="763c5-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="763c5-111">InfrastructurEncryption può essere impostato solo la prima volta che un utente aggiorna il vault CMK.</span><span class="sxs-lookup"><span data-stu-id="763c5-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="763c5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="763c5-112">EXAMPLES</span></span>

### <span data-ttu-id="763c5-113">Esempio 1: Aggiornare SoftDeleteFeatureState di un vault</span><span class="sxs-lookup"><span data-stu-id="763c5-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="763c5-114">Il primo comando ottiene un oggetto Vault e quindi lo archivia nella $vault variabile.</span><span class="sxs-lookup"><span data-stu-id="763c5-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="763c5-115">Il secondo comando aggiorna la proprietà SoftDeleteFeatureState del vault allo stato "Abilitato".</span><span class="sxs-lookup"><span data-stu-id="763c5-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="763c5-116">Esempio 2: Aggiornare la crittografia CMK di un vault</span><span class="sxs-lookup"><span data-stu-id="763c5-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="763c5-117">Il primo cmdlet recupera RSVault per aggiornare le proprietà di crittografia.</span><span class="sxs-lookup"><span data-stu-id="763c5-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="763c5-118">Il secondo cmdlet ottiene il vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="763c5-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="763c5-119">Il terzo cmdlet recupera la chiave dal vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="763c5-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="763c5-120">Il quarto cmdlet aggiorna la chiave di crittografia gestita dal cliente all'interno di RSVault.</span><span class="sxs-lookup"><span data-stu-id="763c5-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="763c5-121">Usare il parametro -InfrastructureEncryption per abilitare la crittografia dell'infrastruttura per il primo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="763c5-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="763c5-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="763c5-122">PARAMETERS</span></span>

### <span data-ttu-id="763c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="763c5-123">-DefaultProfile</span></span>
<span data-ttu-id="763c5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="763c5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="763c5-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="763c5-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="763c5-126">SoftDeleteFeatureState del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="763c5-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="763c5-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="763c5-127">-EncryptionKeyId</span></span>
<span data-ttu-id="763c5-128">KeyId della chiave di crittografia da usare per CMK.</span><span class="sxs-lookup"><span data-stu-id="763c5-128">KeyId of the encryption key to be used for CMK.</span></span>

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

### <span data-ttu-id="763c5-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="763c5-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="763c5-130">ID sottoscrizione del Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="763c5-130">Subscription Id of the Key Vault.</span></span>

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

### <span data-ttu-id="763c5-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="763c5-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="763c5-132">Abilita la crittografia dell'infrastruttura nel Vault.</span><span class="sxs-lookup"><span data-stu-id="763c5-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="763c5-133">La crittografia dell'infrastruttura deve essere abilitata durante la configurazione della crittografia.</span><span class="sxs-lookup"><span data-stu-id="763c5-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

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

### <span data-ttu-id="763c5-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="763c5-134">-VaultId</span></span>
<span data-ttu-id="763c5-135">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="763c5-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="763c5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="763c5-136">-Confirm</span></span>
<span data-ttu-id="763c5-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="763c5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="763c5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="763c5-138">-WhatIf</span></span>
<span data-ttu-id="763c5-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="763c5-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="763c5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="763c5-140">CommonParameters</span></span>
<span data-ttu-id="763c5-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="763c5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="763c5-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="763c5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="763c5-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="763c5-143">INPUTS</span></span>

### <span data-ttu-id="763c5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="763c5-144">System.String</span></span>

### <span data-ttu-id="763c5-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="763c5-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="763c5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="763c5-146">OUTPUTS</span></span>

### <span data-ttu-id="763c5-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="763c5-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="763c5-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="763c5-148">NOTES</span></span>

## <span data-ttu-id="763c5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="763c5-149">RELATED LINKS</span></span>

[<span data-ttu-id="763c5-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="763c5-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="763c5-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="763c5-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
