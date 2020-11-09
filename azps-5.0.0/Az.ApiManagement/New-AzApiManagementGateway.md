---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296587"
---
# <span data-ttu-id="96e6b-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="96e6b-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="96e6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="96e6b-103">Crea una nuova entità gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="96e6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96e6b-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="96e6b-106">Il cmdlet **New-AzApiManagementGateway** crea una nuova entità gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="96e6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96e6b-107">EXAMPLES</span></span>

### <span data-ttu-id="96e6b-108">Esempio 1: creare un gateway</span><span class="sxs-lookup"><span data-stu-id="96e6b-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="96e6b-109">Questo comando crea un gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-109">This command creates a gateway.</span></span>

## <span data-ttu-id="96e6b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96e6b-110">PARAMETERS</span></span>

### <span data-ttu-id="96e6b-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="96e6b-111">-Context</span></span>
<span data-ttu-id="96e6b-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="96e6b-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="96e6b-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="96e6b-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e6b-114">-DefaultProfile</span></span>
<span data-ttu-id="96e6b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96e6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e6b-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="96e6b-116">-Description</span></span>
<span data-ttu-id="96e6b-117">Descrizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-117">Gateway description.</span></span>
<span data-ttu-id="96e6b-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="96e6b-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e6b-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="96e6b-119">-GatewayId</span></span>
<span data-ttu-id="96e6b-120">Identificatore del nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-120">Identifier of new gateway.</span></span>
<span data-ttu-id="96e6b-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="96e6b-121">This parameter is optional.</span></span>
<span data-ttu-id="96e6b-122">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="96e6b-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e6b-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="96e6b-123">-LocationData</span></span>
<span data-ttu-id="96e6b-124">Posizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="96e6b-124">Gateway location.</span></span>
<span data-ttu-id="96e6b-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="96e6b-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e6b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="96e6b-126">-Confirm</span></span>
<span data-ttu-id="96e6b-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e6b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e6b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e6b-128">-WhatIf</span></span>
<span data-ttu-id="96e6b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96e6b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96e6b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96e6b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e6b-131">CommonParameters</span></span>
<span data-ttu-id="96e6b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e6b-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96e6b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e6b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96e6b-134">INPUTS</span></span>

### <span data-ttu-id="96e6b-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="96e6b-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="96e6b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="96e6b-136">System.String</span></span>

### <span data-ttu-id="96e6b-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="96e6b-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="96e6b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96e6b-138">OUTPUTS</span></span>

### <span data-ttu-id="96e6b-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="96e6b-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="96e6b-140">Note</span><span class="sxs-lookup"><span data-stu-id="96e6b-140">NOTES</span></span>

## <span data-ttu-id="96e6b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96e6b-141">RELATED LINKS</span></span>
