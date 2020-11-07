---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520620"
---
# <span data-ttu-id="53509-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="53509-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="53509-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53509-102">SYNOPSIS</span></span>
<span data-ttu-id="53509-103">Rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="53509-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53509-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53509-104">SYNTAX</span></span>

### <span data-ttu-id="53509-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53509-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53509-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="53509-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53509-107">ByName</span><span class="sxs-lookup"><span data-stu-id="53509-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53509-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53509-108">DESCRIPTION</span></span>
<span data-ttu-id="53509-109">Il cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="53509-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="53509-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53509-110">EXAMPLES</span></span>

### <span data-ttu-id="53509-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53509-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="53509-112">Rimuove il server vCenter dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="53509-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="53509-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53509-113">PARAMETERS</span></span>

### <span data-ttu-id="53509-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53509-114">-DefaultProfile</span></span>
<span data-ttu-id="53509-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53509-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53509-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="53509-116">-Fabric</span></span>
<span data-ttu-id="53509-117">Oggetto del tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="53509-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="53509-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53509-118">-InputObject</span></span>
<span data-ttu-id="53509-119">Oggetto VirtualCenter di ASR che rappresenta il server vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="53509-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="53509-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="53509-120">-Name</span></span>
<span data-ttu-id="53509-121">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="53509-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="53509-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53509-122">-ResourceId</span></span>
<span data-ttu-id="53509-123">Specifica il resourceId di vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="53509-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="53509-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53509-124">-Confirm</span></span>
<span data-ttu-id="53509-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53509-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53509-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53509-126">-WhatIf</span></span>
<span data-ttu-id="53509-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53509-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53509-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53509-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53509-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53509-129">CommonParameters</span></span>
<span data-ttu-id="53509-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53509-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53509-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53509-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53509-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53509-132">INPUTS</span></span>

### <span data-ttu-id="53509-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="53509-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="53509-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53509-134">OUTPUTS</span></span>

### <span data-ttu-id="53509-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="53509-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="53509-136">Note</span><span class="sxs-lookup"><span data-stu-id="53509-136">NOTES</span></span>

## <span data-ttu-id="53509-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53509-137">RELATED LINKS</span></span>