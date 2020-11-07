---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677582"
---
# <span data-ttu-id="50499-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="50499-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="50499-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50499-102">SYNOPSIS</span></span>
<span data-ttu-id="50499-103">Rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="50499-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="50499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50499-104">SYNTAX</span></span>

### <span data-ttu-id="50499-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50499-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50499-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50499-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50499-107">ByName</span><span class="sxs-lookup"><span data-stu-id="50499-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50499-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50499-108">DESCRIPTION</span></span>
<span data-ttu-id="50499-109">Il cmdlet **Remove-AzRecoveryServicesAsrvCenter** rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="50499-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="50499-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50499-110">EXAMPLES</span></span>

### <span data-ttu-id="50499-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50499-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="50499-112">Rimuove il server vCenter dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="50499-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="50499-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50499-113">PARAMETERS</span></span>

### <span data-ttu-id="50499-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50499-114">-DefaultProfile</span></span>
<span data-ttu-id="50499-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50499-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50499-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="50499-116">-Fabric</span></span>
<span data-ttu-id="50499-117">Oggetto del tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="50499-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50499-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50499-118">-InputObject</span></span>
<span data-ttu-id="50499-119">Oggetto VirtualCenter di ASR che rappresenta il server vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="50499-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50499-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="50499-120">-Name</span></span>
<span data-ttu-id="50499-121">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="50499-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50499-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50499-122">-ResourceId</span></span>
<span data-ttu-id="50499-123">Specifica il resourceId di vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="50499-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50499-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50499-124">-Confirm</span></span>
<span data-ttu-id="50499-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50499-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50499-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50499-126">-WhatIf</span></span>
<span data-ttu-id="50499-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50499-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50499-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50499-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50499-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50499-129">CommonParameters</span></span>
<span data-ttu-id="50499-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50499-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50499-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50499-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50499-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50499-132">INPUTS</span></span>

### <span data-ttu-id="50499-133">System. String</span><span class="sxs-lookup"><span data-stu-id="50499-133">System.String</span></span>

### <span data-ttu-id="50499-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="50499-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="50499-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="50499-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="50499-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50499-136">OUTPUTS</span></span>

### <span data-ttu-id="50499-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="50499-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="50499-138">Note</span><span class="sxs-lookup"><span data-stu-id="50499-138">NOTES</span></span>

## <span data-ttu-id="50499-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50499-139">RELATED LINKS</span></span>
