---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958494"
---
# <span data-ttu-id="15b43-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="15b43-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="15b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15b43-102">SYNOPSIS</span></span>
<span data-ttu-id="15b43-103">Creare un oggetto di destinazione di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="15b43-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="15b43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15b43-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b43-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15b43-105">DESCRIPTION</span></span>
<span data-ttu-id="15b43-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject crea l'oggetto di destinazione di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="15b43-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="15b43-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15b43-107">EXAMPLES</span></span>

### <span data-ttu-id="15b43-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15b43-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="15b43-109">Tipo: "area di lavoro" WorkspaceSettings: { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="15b43-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="15b43-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15b43-110">PARAMETERS</span></span>

### <span data-ttu-id="15b43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b43-111">-DefaultProfile</span></span>
<span data-ttu-id="15b43-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15b43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15b43-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="15b43-113">-OutputType</span></span>
<span data-ttu-id="15b43-114">Tipo di destinazione di output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="15b43-114">Connection monitor output destination type.</span></span> <span data-ttu-id="15b43-115">Attualmente è supportata \" solo \" l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="15b43-115">Currently, only \"Workspace\" is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b43-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="15b43-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="15b43-117">ID risorsa area di lavoro analisi log.</span><span class="sxs-lookup"><span data-stu-id="15b43-117">Log analytics workspace resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b43-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15b43-118">-Confirm</span></span>
<span data-ttu-id="15b43-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b43-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b43-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b43-120">-WhatIf</span></span>
<span data-ttu-id="15b43-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b43-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b43-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15b43-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b43-123">CommonParameters</span></span>
<span data-ttu-id="15b43-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b43-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15b43-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b43-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="15b43-126">INPUTS</span></span>

### <span data-ttu-id="15b43-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="15b43-127">None</span></span>

## <span data-ttu-id="15b43-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15b43-128">OUTPUTS</span></span>

### <span data-ttu-id="15b43-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="15b43-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="15b43-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="15b43-130">NOTES</span></span>

## <span data-ttu-id="15b43-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15b43-131">RELATED LINKS</span></span>
