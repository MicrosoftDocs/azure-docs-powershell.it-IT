---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514216"
---
# <span data-ttu-id="dcc9f-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="dcc9f-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="dcc9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc9f-103">Rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcc9f-104">SYNTAX</span></span>

### <span data-ttu-id="dcc9f-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcc9f-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc9f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc9f-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcc9f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="dcc9f-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcc9f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcc9f-108">DESCRIPTION</span></span>
<span data-ttu-id="dcc9f-109">Il cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** rimuove il server vCenter dal tessuto ASR e interrompe l'individuazione delle macchine virtuali dal server vCenter.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="dcc9f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcc9f-110">EXAMPLES</span></span>

### <span data-ttu-id="dcc9f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dcc9f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="dcc9f-112">Rimuove il server vCenter dal tessuto ASR.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="dcc9f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcc9f-113">PARAMETERS</span></span>

### <span data-ttu-id="dcc9f-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dcc9f-114">-Confirm</span></span>
<span data-ttu-id="dcc9f-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcc9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc9f-116">-DefaultProfile</span></span>
<span data-ttu-id="dcc9f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcc9f-118">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="dcc9f-118">-Fabric</span></span>
<span data-ttu-id="dcc9f-119">Oggetto del tessuto ASR che rappresenta il server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcc9f-120">-InputObject</span></span>
<span data-ttu-id="dcc9f-121">Oggetto VirtualCenter di ASR che rappresenta il server vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcc9f-122">-Name</span></span>
<span data-ttu-id="dcc9f-123">Nome del server vCenter.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcc9f-124">-ResourceId</span></span>
<span data-ttu-id="dcc9f-125">Specifica il resourceId di vCenter da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc9f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc9f-126">-WhatIf</span></span>
<span data-ttu-id="dcc9f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc9f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcc9f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc9f-129">CommonParameters</span></span>
<span data-ttu-id="dcc9f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcc9f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc9f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc9f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc9f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcc9f-132">INPUTS</span></span>

### <span data-ttu-id="dcc9f-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="dcc9f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="dcc9f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcc9f-134">OUTPUTS</span></span>

### <span data-ttu-id="dcc9f-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dcc9f-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dcc9f-136">Note</span><span class="sxs-lookup"><span data-stu-id="dcc9f-136">NOTES</span></span>

## <span data-ttu-id="dcc9f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcc9f-137">RELATED LINKS</span></span>
