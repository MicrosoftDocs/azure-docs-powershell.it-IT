---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 19395960d3a0026b7a14c4ca8232c18d511af989
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676085"
---
# <span data-ttu-id="c4bf4-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c4bf4-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c4bf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bf4-103">Ottenere la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-103">Get the API Release.</span></span>

## <span data-ttu-id="c4bf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4bf4-104">SYNTAX</span></span>

### <span data-ttu-id="c4bf4-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4bf4-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4bf4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4bf4-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4bf4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="c4bf4-108">Il cmdlet **Get-AzApiManagementApiRelease** ottiene una o più versioni dell'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="c4bf4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="c4bf4-110">Esempio 1: ottenere tutte le versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="c4bf4-110">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="c4bf4-111">Questo comando consente di ottenere tutte le versioni dell' `echo-api` API per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="c4bf4-112">Esempio 2: ottenere le informazioni sulla versione della versione specifica dell'API</span><span class="sxs-lookup"><span data-stu-id="c4bf4-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="c4bf4-113">Questo comando consente di ottenere le informazioni sulle versioni di una specifica API con il releaseId specificato.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="c4bf4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4bf4-114">PARAMETERS</span></span>

### <span data-ttu-id="c4bf4-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c4bf4-115">-ApiId</span></span>
<span data-ttu-id="c4bf4-116">Identificatore API da cercare.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-116">API identifier to look for.</span></span>
<span data-ttu-id="c4bf4-117">Se specificato cercherà di ottenere l'API dall'ID.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf4-118">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c4bf4-118">-Context</span></span>
<span data-ttu-id="c4bf4-119">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c4bf4-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bf4-121">-DefaultProfile</span></span>
<span data-ttu-id="c4bf4-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bf4-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c4bf4-123">-ReleaseId</span></span>
<span data-ttu-id="c4bf4-124">Identificatore della versione.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bf4-125">-ResourceId</span></span>
<span data-ttu-id="c4bf4-126">Identificatore delle risorse ARM di una versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="c4bf4-127">Se specificato cercherà di trovare il rilascio dell'API dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="c4bf4-128">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bf4-129">CommonParameters</span></span>
<span data-ttu-id="c4bf4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bf4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bf4-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4bf4-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bf4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4bf4-132">INPUTS</span></span>

### <span data-ttu-id="c4bf4-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c4bf4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c4bf4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c4bf4-134">System.String</span></span>

## <span data-ttu-id="c4bf4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4bf4-135">OUTPUTS</span></span>

### <span data-ttu-id="c4bf4-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c4bf4-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c4bf4-137">Note</span><span class="sxs-lookup"><span data-stu-id="c4bf4-137">NOTES</span></span>

## <span data-ttu-id="c4bf4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4bf4-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4bf4-139">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c4bf4-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c4bf4-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c4bf4-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="c4bf4-141">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c4bf4-141">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)