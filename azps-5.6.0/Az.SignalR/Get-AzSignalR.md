---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: e7287cff34420c7885f5cddef95e4ca3b09e881f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955502"
---
# <span data-ttu-id="849c7-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="849c7-101">Get-AzSignalR</span></span>

## <span data-ttu-id="849c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="849c7-102">SYNOPSIS</span></span>
<span data-ttu-id="849c7-103">Ottieni un servizio SignalR specifico o tutti i servizi SignalR in un gruppo di risorse o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="849c7-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="849c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="849c7-104">SYNTAX</span></span>

### <span data-ttu-id="849c7-105">ListSignalRServiceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="849c7-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="849c7-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="849c7-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="849c7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="849c7-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849c7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="849c7-108">DESCRIPTION</span></span>
<span data-ttu-id="849c7-109">Ottieni un servizio SignalR specifico o tutti i servizi SignalR in un gruppo di risorse o un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="849c7-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="849c7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="849c7-110">EXAMPLES</span></span>

### <span data-ttu-id="849c7-111">Scarica tutti i servizi SignalR nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="849c7-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="849c7-112">Ottenere tutti i servizi SignalR in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="849c7-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="849c7-113">Ottieni un servizio SignalR specifico</span><span class="sxs-lookup"><span data-stu-id="849c7-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="849c7-114">Ottenere un servizio SignalR specifico dal gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="849c7-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="849c7-115">Il gruppo di risorse predefinito può essere impostato \` da Set-AzDefault -ResourceGroupName \` myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="849c7-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="849c7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="849c7-116">PARAMETERS</span></span>

### <span data-ttu-id="849c7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849c7-117">-DefaultProfile</span></span>
<span data-ttu-id="849c7-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="849c7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="849c7-119">-Name</span></span>
<span data-ttu-id="849c7-120">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="849c7-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849c7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849c7-121">-ResourceGroupName</span></span>
<span data-ttu-id="849c7-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="849c7-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849c7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="849c7-123">-ResourceId</span></span>
<span data-ttu-id="849c7-124">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="849c7-124">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="849c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849c7-125">CommonParameters</span></span>
<span data-ttu-id="849c7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849c7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="849c7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849c7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="849c7-128">INPUTS</span></span>

### <span data-ttu-id="849c7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="849c7-129">System.String</span></span>
## <span data-ttu-id="849c7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="849c7-130">OUTPUTS</span></span>

### <span data-ttu-id="849c7-131">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="849c7-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="849c7-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="849c7-132">NOTES</span></span>

## <span data-ttu-id="849c7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="849c7-133">RELATED LINKS</span></span>
