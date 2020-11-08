---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 4b34bdf2357b389081297df8f49745127953985b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191971"
---
# <span data-ttu-id="8acec-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8acec-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="8acec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8acec-102">SYNOPSIS</span></span>
<span data-ttu-id="8acec-103">Aggiorna le proprietà di un Vault.</span><span class="sxs-lookup"><span data-stu-id="8acec-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="8acec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8acec-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8acec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8acec-105">DESCRIPTION</span></span>
<span data-ttu-id="8acec-106">Il cmdlet **set-AzRecoveryServicesVaultProperty** aggiorna le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8acec-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="8acec-107">Questo cmdlet restituisce le proprietà di Vault aggiornate dopo l'operazione di set corrente.</span><span class="sxs-lookup"><span data-stu-id="8acec-107">This cmdlet returns the updated vault properties after the current set operation.</span></span>
<span data-ttu-id="8acec-108">L'uso di queste proprietà cmdlet di Vault, ad esempio soft-delete, può essere abilitato in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="8acec-108">Using this cmdlet properties of vault such as soft-delete can be enabled at any point of time.</span></span>
<span data-ttu-id="8acec-109">La proprietà **SoftDeleteFeatureState** di un Vault può essere disabilitata solo se non sono presenti contenitori registrati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="8acec-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>

## <span data-ttu-id="8acec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8acec-110">EXAMPLES</span></span>

### <span data-ttu-id="8acec-111">Esempio 1: aggiornare SoftDeleteFeatureState di un Vault</span><span class="sxs-lookup"><span data-stu-id="8acec-111">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="8acec-112">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="8acec-112">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="8acec-113">Il secondo comando Aggiorna la proprietà SoftDeleteFeatureState della volta in stato "Enabled".</span><span class="sxs-lookup"><span data-stu-id="8acec-113">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="8acec-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8acec-114">PARAMETERS</span></span>

### <span data-ttu-id="8acec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acec-115">-DefaultProfile</span></span>
<span data-ttu-id="8acec-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8acec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acec-117">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8acec-117">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="8acec-118">SoftDeleteFeatureState del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8acec-118">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8acec-119">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8acec-119">-VaultId</span></span>
<span data-ttu-id="8acec-120">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="8acec-120">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8acec-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8acec-121">-Confirm</span></span>
<span data-ttu-id="8acec-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8acec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8acec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8acec-123">-WhatIf</span></span>
<span data-ttu-id="8acec-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8acec-124">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="8acec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acec-125">CommonParameters</span></span>
<span data-ttu-id="8acec-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8acec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acec-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8acec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acec-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8acec-128">INPUTS</span></span>

### <span data-ttu-id="8acec-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8acec-129">System.String</span></span>

### <span data-ttu-id="8acec-130">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="8acec-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="8acec-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8acec-131">OUTPUTS</span></span>

### <span data-ttu-id="8acec-132">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="8acec-132">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="8acec-133">Note</span><span class="sxs-lookup"><span data-stu-id="8acec-133">NOTES</span></span>

## <span data-ttu-id="8acec-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8acec-134">RELATED LINKS</span></span>

[<span data-ttu-id="8acec-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8acec-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="8acec-136">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="8acec-136">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


