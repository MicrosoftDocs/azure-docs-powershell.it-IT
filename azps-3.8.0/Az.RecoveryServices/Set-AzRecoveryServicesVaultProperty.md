---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a9bd1eead98a7afb06e1f5b480f8a65fc5079bd4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021479"
---
# <span data-ttu-id="03307-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="03307-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="03307-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03307-102">SYNOPSIS</span></span>
<span data-ttu-id="03307-103">Aggiorna le proprietà di un Vault.</span><span class="sxs-lookup"><span data-stu-id="03307-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="03307-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03307-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03307-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03307-105">DESCRIPTION</span></span>
<span data-ttu-id="03307-106">Il cmdlet **set-AzRecoveryServicesVaultProperty** aggiorna le proprietà di un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="03307-106">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span>
<span data-ttu-id="03307-107">Puoi usare il cmdlet **set-AzRecoveryServicesVaultProperty** per ottenere le proprietà correnti di un Vault.</span><span class="sxs-lookup"><span data-stu-id="03307-107">You can use **Set-AzRecoveryServicesVaultProperty** cmdlet to get the current properties of a vault.</span></span>
<span data-ttu-id="03307-108">L'uso di questo cmdlet **SoftDeleteFeatureState** proprietà di un Vault può essere abilitato in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="03307-108">Using this cmdlet **SoftDeleteFeatureState** property of a vault can be enabled at any point of time.</span></span>
<span data-ttu-id="03307-109">La proprietà **SoftDeleteFeatureState** di un Vault può essere disabilitata solo se non sono presenti contenitori registrati nel Vault.</span><span class="sxs-lookup"><span data-stu-id="03307-109">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span>
<span data-ttu-id="03307-110">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="03307-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="03307-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03307-111">EXAMPLES</span></span>

### <span data-ttu-id="03307-112">Esempio 1: aggiornare SoftDeleteFeatureState di un Vault</span><span class="sxs-lookup"><span data-stu-id="03307-112">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="03307-113">Il primo comando ottiene un oggetto Vault e lo archivia nella variabile $vault.</span><span class="sxs-lookup"><span data-stu-id="03307-113">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="03307-114">Il secondo comando Aggiorna la proprietà SoftDeleteFeatureState della volta in stato "Enabled".</span><span class="sxs-lookup"><span data-stu-id="03307-114">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

## <span data-ttu-id="03307-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03307-115">PARAMETERS</span></span>

### <span data-ttu-id="03307-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03307-116">-DefaultProfile</span></span>
<span data-ttu-id="03307-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03307-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03307-118">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="03307-118">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="03307-119">SoftDeleteFeatureState del Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="03307-119">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="03307-120">-VaultId</span><span class="sxs-lookup"><span data-stu-id="03307-120">-VaultId</span></span>
<span data-ttu-id="03307-121">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="03307-121">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="03307-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03307-122">-Confirm</span></span>
<span data-ttu-id="03307-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03307-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03307-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03307-124">-WhatIf</span></span>
<span data-ttu-id="03307-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03307-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03307-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03307-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03307-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03307-127">CommonParameters</span></span>
<span data-ttu-id="03307-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03307-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03307-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03307-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03307-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03307-130">INPUTS</span></span>

### <span data-ttu-id="03307-131">System. String</span><span class="sxs-lookup"><span data-stu-id="03307-131">System.String</span></span>

### <span data-ttu-id="03307-132">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="03307-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="03307-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03307-133">OUTPUTS</span></span>

### <span data-ttu-id="03307-134">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="03307-134">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="03307-135">Note</span><span class="sxs-lookup"><span data-stu-id="03307-135">NOTES</span></span>

## <span data-ttu-id="03307-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03307-136">RELATED LINKS</span></span>

[<span data-ttu-id="03307-137">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03307-137">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="03307-138">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="03307-138">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)


