---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalR.md
ms.openlocfilehash: f739c5fa018a4d4f4ebf553c76dbacd35ee315c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191905"
---
# <span data-ttu-id="38644-101">Get-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="38644-101">Get-AzSignalR</span></span>

## <span data-ttu-id="38644-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38644-102">SYNOPSIS</span></span>
<span data-ttu-id="38644-103">Ottenere un servizio di segnalazione specifico o tutti i servizi di segnalazione in un gruppo di risorse o in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="38644-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="38644-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38644-104">SYNTAX</span></span>

### <span data-ttu-id="38644-105">ListSignalRServiceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38644-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38644-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="38644-106">ResourceGroupParameterSet</span></span>
```
Get-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38644-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38644-107">ResourceIdParameterSet</span></span>
```
Get-AzSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38644-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38644-108">DESCRIPTION</span></span>
<span data-ttu-id="38644-109">Ottenere un servizio di segnalazione specifico o tutti i servizi di segnalazione in un gruppo di risorse o in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="38644-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="38644-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38644-110">EXAMPLES</span></span>

### <span data-ttu-id="38644-111">Ottenere tutti i servizi di segnalazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="38644-111">Get all SignalR services in the subscription</span></span>
```
PS C:\> Get-AzSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="38644-112">Ottenere tutti i servizi di SignalR in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="38644-112">Get all SignalR services in a resource group</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="38644-113">Ottenere un servizio di segnalazione specifico</span><span class="sxs-lookup"><span data-stu-id="38644-113">Get a specific SignalR service</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="38644-114">Ottenere un servizio di segnalazione specifico dal gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="38644-114">Get a specific SignalR service from the default resource group</span></span>
```
PS C:\> Get-AzSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="38644-115">Il gruppo di risorse predefinito può essere impostato da \` set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="38644-115">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="38644-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38644-116">PARAMETERS</span></span>

### <span data-ttu-id="38644-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38644-117">-DefaultProfile</span></span>
<span data-ttu-id="38644-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38644-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38644-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="38644-119">-Name</span></span>
<span data-ttu-id="38644-120">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="38644-120">SignalR service name.</span></span>

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

### <span data-ttu-id="38644-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38644-121">-ResourceGroupName</span></span>
<span data-ttu-id="38644-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38644-122">Resource group name.</span></span>

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

### <span data-ttu-id="38644-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38644-123">-ResourceId</span></span>
<span data-ttu-id="38644-124">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="38644-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="38644-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38644-125">CommonParameters</span></span>
<span data-ttu-id="38644-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38644-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38644-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38644-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38644-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38644-128">INPUTS</span></span>

### <span data-ttu-id="38644-129">System. String</span><span class="sxs-lookup"><span data-stu-id="38644-129">System.String</span></span>
## <span data-ttu-id="38644-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38644-130">OUTPUTS</span></span>

### <span data-ttu-id="38644-131">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="38644-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="38644-132">Note</span><span class="sxs-lookup"><span data-stu-id="38644-132">NOTES</span></span>

## <span data-ttu-id="38644-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38644-133">RELATED LINKS</span></span>
