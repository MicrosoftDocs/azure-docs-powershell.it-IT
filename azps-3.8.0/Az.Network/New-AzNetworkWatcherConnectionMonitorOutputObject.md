---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018978"
---
# <span data-ttu-id="82331-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="82331-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="82331-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82331-102">SYNOPSIS</span></span>
<span data-ttu-id="82331-103">Creare un oggetto di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="82331-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="82331-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82331-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82331-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82331-105">DESCRIPTION</span></span>
<span data-ttu-id="82331-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject crea l'oggetto di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="82331-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="82331-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82331-107">EXAMPLES</span></span>

### <span data-ttu-id="82331-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82331-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="82331-109">Digitare: "area di lavoro" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="82331-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="82331-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82331-110">PARAMETERS</span></span>

### <span data-ttu-id="82331-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82331-111">-DefaultProfile</span></span>
<span data-ttu-id="82331-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82331-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82331-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="82331-113">-OutputType</span></span>
<span data-ttu-id="82331-114">Tipo di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="82331-114">Connection monitor output destination type.</span></span> <span data-ttu-id="82331-115">Attualmente \" è supportata solo l'area di lavoro \" .</span><span class="sxs-lookup"><span data-stu-id="82331-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="82331-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="82331-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="82331-117">ID risorsa log dell'area di lavoro analisi.</span><span class="sxs-lookup"><span data-stu-id="82331-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="82331-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82331-118">-Confirm</span></span>
<span data-ttu-id="82331-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82331-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82331-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82331-120">-WhatIf</span></span>
<span data-ttu-id="82331-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82331-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82331-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82331-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82331-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82331-123">CommonParameters</span></span>
<span data-ttu-id="82331-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82331-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82331-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82331-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82331-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82331-126">INPUTS</span></span>

### <span data-ttu-id="82331-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82331-127">None</span></span>

## <span data-ttu-id="82331-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82331-128">OUTPUTS</span></span>

### <span data-ttu-id="82331-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="82331-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="82331-130">Note</span><span class="sxs-lookup"><span data-stu-id="82331-130">NOTES</span></span>

## <span data-ttu-id="82331-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82331-131">RELATED LINKS</span></span>
