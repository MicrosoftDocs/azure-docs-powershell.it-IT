---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372203"
---
# <span data-ttu-id="839cb-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="839cb-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="839cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="839cb-102">SYNOPSIS</span></span>
<span data-ttu-id="839cb-103">Creare un oggetto di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="839cb-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="839cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="839cb-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="839cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="839cb-105">DESCRIPTION</span></span>
<span data-ttu-id="839cb-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorOutputObject crea l'oggetto di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="839cb-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="839cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="839cb-107">EXAMPLES</span></span>

### <span data-ttu-id="839cb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="839cb-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="839cb-109">Digitare: "area di lavoro" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="839cb-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="839cb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="839cb-110">PARAMETERS</span></span>

### <span data-ttu-id="839cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839cb-111">-DefaultProfile</span></span>
<span data-ttu-id="839cb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="839cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="839cb-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="839cb-113">-OutputType</span></span>
<span data-ttu-id="839cb-114">Tipo di destinazione dell'output del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="839cb-114">Connection monitor output destination type.</span></span> <span data-ttu-id="839cb-115">Attualmente \" è supportata solo l'area di lavoro \" .</span><span class="sxs-lookup"><span data-stu-id="839cb-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="839cb-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="839cb-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="839cb-117">ID risorsa log dell'area di lavoro analisi.</span><span class="sxs-lookup"><span data-stu-id="839cb-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="839cb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="839cb-118">-Confirm</span></span>
<span data-ttu-id="839cb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="839cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="839cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839cb-120">-WhatIf</span></span>
<span data-ttu-id="839cb-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="839cb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="839cb-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="839cb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="839cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839cb-123">CommonParameters</span></span>
<span data-ttu-id="839cb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839cb-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="839cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839cb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="839cb-126">INPUTS</span></span>

### <span data-ttu-id="839cb-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="839cb-127">None</span></span>

## <span data-ttu-id="839cb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="839cb-128">OUTPUTS</span></span>

### <span data-ttu-id="839cb-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="839cb-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="839cb-130">Note</span><span class="sxs-lookup"><span data-stu-id="839cb-130">NOTES</span></span>

## <span data-ttu-id="839cb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="839cb-131">RELATED LINKS</span></span>
