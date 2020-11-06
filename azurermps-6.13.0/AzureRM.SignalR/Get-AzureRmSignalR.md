---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalR.md
ms.openlocfilehash: 08e68a878267f706c280c8d461e8c904141cd06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516440"
---
# <span data-ttu-id="b11b9-101">Get-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="b11b9-101">Get-AzureRmSignalR</span></span>

## <span data-ttu-id="b11b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b11b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b11b9-103">Ottenere un servizio di segnalazione specifico o tutti i servizi di segnalazione in un gruppo di risorse o in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b11b9-103">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b11b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b11b9-104">SYNTAX</span></span>

### <span data-ttu-id="b11b9-105">ListSignalRServiceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b11b9-105">ListSignalRServiceParameterSet (Default)</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b11b9-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b11b9-106">ResourceGroupParameterSet</span></span>
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b11b9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b11b9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b11b9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b11b9-108">DESCRIPTION</span></span>
<span data-ttu-id="b11b9-109">Ottenere un servizio di segnalazione specifico o tutti i servizi di segnalazione in un gruppo di risorse o in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b11b9-109">Get a specific SignalR service or all the SignalR services in a resource group or a subscription.</span></span>

## <span data-ttu-id="b11b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b11b9-110">EXAMPLES</span></span>

### <span data-ttu-id="b11b9-111">Ottenere tutti i servizi di segnalazione nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="b11b9-111">Get all SignalR services in the subscription</span></span>
```powershell
PS C:\> Get-AzureRmSignalR


HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr3.service.signalr.net                     eastus         5002       5001       Creating          1.0
```

### <span data-ttu-id="b11b9-112">Ottenere tutti i servizi di SignalR in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b11b9-112">Get all SignalR services in a resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="b11b9-113">Ottenere un servizio di segnalazione specifico</span><span class="sxs-lookup"><span data-stu-id="b11b9-113">Get a specific SignalR service</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

### <span data-ttu-id="b11b9-114">Ottenere un servizio di segnalazione specifico dal gruppo di risorse predefinito</span><span class="sxs-lookup"><span data-stu-id="b11b9-114">Get a specific SignalR service from the default resource group</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr2.service.signalr.net                     eastus         5002       5001       Succeeded         1.0
```

<span data-ttu-id="b11b9-115">Il gruppo di risorse predefinito può essere impostato da `Set-AzureRmDefault -ResourceGroupName myResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="b11b9-115">The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.</span></span>

## <span data-ttu-id="b11b9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b11b9-116">PARAMETERS</span></span>

### <span data-ttu-id="b11b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b11b9-117">-DefaultProfile</span></span>
<span data-ttu-id="b11b9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b11b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b11b9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b11b9-119">-Name</span></span>
<span data-ttu-id="b11b9-120">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="b11b9-120">SignalR service name.</span></span>

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

### <span data-ttu-id="b11b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b11b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="b11b9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b11b9-122">Resource group name.</span></span>

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

### <span data-ttu-id="b11b9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b11b9-123">-ResourceId</span></span>
<span data-ttu-id="b11b9-124">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="b11b9-124">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b11b9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b11b9-125">CommonParameters</span></span>
<span data-ttu-id="b11b9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b11b9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b11b9-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b11b9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b11b9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b11b9-128">INPUTS</span></span>

### <span data-ttu-id="b11b9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b11b9-129">System.String</span></span>
<span data-ttu-id="b11b9-130">Parametri: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b11b9-130">Parameters: ResourceId (ByValue)</span></span>

## <span data-ttu-id="b11b9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b11b9-131">OUTPUTS</span></span>

### <span data-ttu-id="b11b9-132">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b11b9-132">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="b11b9-133">Note</span><span class="sxs-lookup"><span data-stu-id="b11b9-133">NOTES</span></span>

## <span data-ttu-id="b11b9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b11b9-134">RELATED LINKS</span></span>
