---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195399"
---
# <span data-ttu-id="c7bbc-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c7bbc-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="c7bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bbc-103">Crea una nuova entità Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="c7bbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7bbc-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bbc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7bbc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bbc-106">Il cmdlet **New-AzApiManagementGateway** crea una nuova entità Gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="c7bbc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7bbc-107">EXAMPLES</span></span>

### <span data-ttu-id="c7bbc-108">Esempio 1: Creare un gateway</span><span class="sxs-lookup"><span data-stu-id="c7bbc-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="c7bbc-109">Questo comando crea un gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-109">This command creates a gateway.</span></span>

## <span data-ttu-id="c7bbc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7bbc-110">PARAMETERS</span></span>

### <span data-ttu-id="c7bbc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c7bbc-111">-Context</span></span>
<span data-ttu-id="c7bbc-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c7bbc-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c7bbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bbc-114">-DefaultProfile</span></span>
<span data-ttu-id="c7bbc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7bbc-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7bbc-116">-Description</span></span>
<span data-ttu-id="c7bbc-117">Descrizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-117">Gateway description.</span></span>
<span data-ttu-id="c7bbc-118">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="c7bbc-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c7bbc-119">-GatewayId</span></span>
<span data-ttu-id="c7bbc-120">Identificatore del nuovo gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-120">Identifier of new gateway.</span></span>
<span data-ttu-id="c7bbc-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-121">This parameter is optional.</span></span>
<span data-ttu-id="c7bbc-122">Se non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="c7bbc-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="c7bbc-123">-LocationData</span></span>
<span data-ttu-id="c7bbc-124">Posizione del gateway.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-124">Gateway location.</span></span>
<span data-ttu-id="c7bbc-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-125">This parameter is required.</span></span>

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

### <span data-ttu-id="c7bbc-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7bbc-126">-Confirm</span></span>
<span data-ttu-id="c7bbc-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bbc-128">-WhatIf</span></span>
<span data-ttu-id="c7bbc-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7bbc-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bbc-131">CommonParameters</span></span>
<span data-ttu-id="c7bbc-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bbc-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7bbc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bbc-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7bbc-134">INPUTS</span></span>

### <span data-ttu-id="c7bbc-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7bbc-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7bbc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c7bbc-136">System.String</span></span>

### <span data-ttu-id="c7bbc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="c7bbc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="c7bbc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7bbc-138">OUTPUTS</span></span>

### <span data-ttu-id="c7bbc-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="c7bbc-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="c7bbc-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7bbc-140">NOTES</span></span>

## <span data-ttu-id="c7bbc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7bbc-141">RELATED LINKS</span></span>
