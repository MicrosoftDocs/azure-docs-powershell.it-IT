---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: e5cb8412836a6b3afc7387d46ef1c68aa699c76a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995775"
---
# <span data-ttu-id="d603b-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="d603b-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="d603b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d603b-102">SYNOPSIS</span></span>
<span data-ttu-id="d603b-103">Recupera un segreto client per il server di autorizzazione gestione API.</span><span class="sxs-lookup"><span data-stu-id="d603b-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="d603b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d603b-104">SYNTAX</span></span>

### <span data-ttu-id="d603b-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d603b-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d603b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d603b-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d603b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d603b-107">DESCRIPTION</span></span>
<span data-ttu-id="d603b-108">Il cmdlet **Get-AzApiManagementAuthorizationServerClientSecret** ottiene il segreto client del server di autorizzazione Gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="d603b-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="d603b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d603b-109">EXAMPLES</span></span>

### <span data-ttu-id="d603b-110">Esempio 1: Ottenere un segreto client del server di autorizzazione specificato in base all'ID</span><span class="sxs-lookup"><span data-stu-id="d603b-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="d603b-111">Questo comando recupera il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d603b-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="d603b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d603b-112">PARAMETERS</span></span>

### <span data-ttu-id="d603b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d603b-113">-Context</span></span>
<span data-ttu-id="d603b-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d603b-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d603b-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d603b-115">This parameter is required.</span></span>

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

### <span data-ttu-id="d603b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d603b-116">-DefaultProfile</span></span>
<span data-ttu-id="d603b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d603b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d603b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d603b-118">-ResourceId</span></span>
<span data-ttu-id="d603b-119">Arm Resource Identifier del server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d603b-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="d603b-120">Se specificato, tenterà di trovare il server di autorizzazione in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d603b-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="d603b-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d603b-121">This parameter is required.</span></span>

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

### <span data-ttu-id="d603b-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="d603b-122">-ServerId</span></span>
<span data-ttu-id="d603b-123">Identificatore del server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="d603b-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="d603b-124">Se specificato, troverà il server di autorizzazione in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d603b-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="d603b-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d603b-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d603b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d603b-126">CommonParameters</span></span>
<span data-ttu-id="d603b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d603b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d603b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d603b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d603b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d603b-129">INPUTS</span></span>

### <span data-ttu-id="d603b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d603b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d603b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d603b-131">System.String</span></span>

## <span data-ttu-id="d603b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d603b-132">OUTPUTS</span></span>

### <span data-ttu-id="d603b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="d603b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="d603b-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="d603b-134">NOTES</span></span>

## <span data-ttu-id="d603b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d603b-135">RELATED LINKS</span></span>
