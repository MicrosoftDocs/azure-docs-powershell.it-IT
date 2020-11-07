---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 921465be93701cbf19b30c661df5a5e3d04413d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686810"
---
# <span data-ttu-id="fe5c1-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="fe5c1-101">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="fe5c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5c1-103">Interrompe la raccolta di dati syslog da computer Linux.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-103">Stops collection of syslog data from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe5c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe5c1-104">SYNTAX</span></span>

### <span data-ttu-id="fe5c1-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe5c1-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe5c1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fe5c1-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe5c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe5c1-107">DESCRIPTION</span></span>
<span data-ttu-id="fe5c1-108">Il cmdlet **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** interrompe la raccolta di dati syslog da computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-108">The **Disable-AzureRmOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fe5c1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe5c1-109">EXAMPLES</span></span>

## <span data-ttu-id="fe5c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe5c1-110">PARAMETERS</span></span>

### <span data-ttu-id="fe5c1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5c1-111">-ResourceGroupName</span></span>
<span data-ttu-id="fe5c1-112">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c1-113">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="fe5c1-113">-Workspace</span></span>
<span data-ttu-id="fe5c1-114">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c1-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe5c1-115">-WorkspaceName</span></span>
<span data-ttu-id="fe5c1-116">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c1-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe5c1-117">-Confirm</span></span>
<span data-ttu-id="fe5c1-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe5c1-119">-WhatIf</span></span>
<span data-ttu-id="fe5c1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe5c1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5c1-122">-DefaultProfile</span></span>
<span data-ttu-id="fe5c1-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe5c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5c1-124">CommonParameters</span></span>
<span data-ttu-id="fe5c1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5c1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe5c1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5c1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe5c1-127">INPUTS</span></span>

### <span data-ttu-id="fe5c1-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fe5c1-128">PSWorkspace</span></span>
<span data-ttu-id="fe5c1-129">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe5c1-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="fe5c1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe5c1-130">OUTPUTS</span></span>

### <span data-ttu-id="fe5c1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fe5c1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fe5c1-132">Note</span><span class="sxs-lookup"><span data-stu-id="fe5c1-132">NOTES</span></span>
* <span data-ttu-id="fe5c1-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="fe5c1-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fe5c1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe5c1-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe5c1-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="fe5c1-135">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="fe5c1-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="fe5c1-136">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzureRmOperationalInsightsLinuxSyslogDataSource.md)


