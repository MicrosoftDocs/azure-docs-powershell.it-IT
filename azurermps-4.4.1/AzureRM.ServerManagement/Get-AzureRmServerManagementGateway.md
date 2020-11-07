---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686153"
---
# <span data-ttu-id="abb39-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="abb39-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="abb39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abb39-102">SYNOPSIS</span></span>
<span data-ttu-id="abb39-103">Ottiene uno o più gateway di gestione dei server.</span><span class="sxs-lookup"><span data-stu-id="abb39-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abb39-104">SYNTAX</span></span>

### <span data-ttu-id="abb39-105">Noparams (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abb39-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb39-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="abb39-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="abb39-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="abb39-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb39-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="abb39-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abb39-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abb39-109">DESCRIPTION</span></span>
<span data-ttu-id="abb39-110">Il cmdlet **Get-AzureRmServerManagementGateway** ottiene uno o più gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="abb39-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="abb39-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abb39-111">EXAMPLES</span></span>

### <span data-ttu-id="abb39-112">Esempio 1: ottenere tutti i gateway in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="abb39-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="abb39-113">Questo comando consente di ottenere tutti i gateway di gestione dei server nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="abb39-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="abb39-114">Esempio 2: ottenere gateway in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="abb39-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="abb39-115">Questo comando consente di ottenere tutti i gateway di gestione dei server appartenenti al gruppo di risorse denominato Group001.</span><span class="sxs-lookup"><span data-stu-id="abb39-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="abb39-116">Esempio 3: ottenere tutte le istanze installate di un gateway</span><span class="sxs-lookup"><span data-stu-id="abb39-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="abb39-117">Questo comando consente di ottenere tutte le istanze di un gateway di gestione del server denominato Gateway01 che appartengono al gruppo di risorse denominato Group002.</span><span class="sxs-lookup"><span data-stu-id="abb39-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="abb39-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abb39-118">PARAMETERS</span></span>

### <span data-ttu-id="abb39-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="abb39-119">-Gateway</span></span>
<span data-ttu-id="abb39-120">Specifica un gateway ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb39-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="abb39-121">Il cmdlet usa i parametri *ResourceGroupName* e *GatewayName* tramite il gateway specificato per eseguire l'azione.</span><span class="sxs-lookup"><span data-stu-id="abb39-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="abb39-122">Quando questo parametro viene specificato, questo cmdlet includerà lo stato dettagliato per il gateway.</span><span class="sxs-lookup"><span data-stu-id="abb39-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb39-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="abb39-123">-GatewayName</span></span>
<span data-ttu-id="abb39-124">Specifica il nome del gateway di gestione del server per il quale questo cmdlet ottiene il Gate.</span><span class="sxs-lookup"><span data-stu-id="abb39-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="abb39-125">Quando specifichi il parametro *GatewayName* , questo cmdlet includerà lo stato dettagliato sul gateway.</span><span class="sxs-lookup"><span data-stu-id="abb39-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb39-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb39-126">-ResourceGroupName</span></span>
<span data-ttu-id="abb39-127">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene i gateway.</span><span class="sxs-lookup"><span data-stu-id="abb39-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb39-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb39-128">-DefaultProfile</span></span>
<span data-ttu-id="abb39-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abb39-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb39-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb39-130">CommonParameters</span></span>
<span data-ttu-id="abb39-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb39-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb39-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb39-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb39-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abb39-133">INPUTS</span></span>

### <span data-ttu-id="abb39-134">Gateway</span><span class="sxs-lookup"><span data-stu-id="abb39-134">Gateway</span></span>
<span data-ttu-id="abb39-135">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="abb39-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="abb39-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abb39-136">OUTPUTS</span></span>

### <span data-ttu-id="abb39-137">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="abb39-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="abb39-138">Note</span><span class="sxs-lookup"><span data-stu-id="abb39-138">NOTES</span></span>
* <span data-ttu-id="abb39-139">Se questo cmdlet viene usato senza parametri, restituirà tutti i gateway associati all'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="abb39-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="abb39-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abb39-140">RELATED LINKS</span></span>

[<span data-ttu-id="abb39-141">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="abb39-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="abb39-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="abb39-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


