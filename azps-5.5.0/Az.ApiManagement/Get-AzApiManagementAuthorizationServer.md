---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192534"
---
# <span data-ttu-id="1ec07-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ec07-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="1ec07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec07-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec07-103">Ottiene un server di autorizzazione gestione API.</span><span class="sxs-lookup"><span data-stu-id="1ec07-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="1ec07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ec07-104">SYNTAX</span></span>

### <span data-ttu-id="1ec07-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ec07-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ec07-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ec07-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec07-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1ec07-107">DESCRIPTION</span></span>
<span data-ttu-id="1ec07-108">Il cmdlet **Get-AzApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione gestione API di Azure o un server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1ec07-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="1ec07-109">ClientSecret non verrà incluso nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="1ec07-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="1ec07-110">Per ottenere il segreto client, usare **Get-AzApiManagementAuthorizationServerClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="1ec07-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="1ec07-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ec07-111">EXAMPLES</span></span>

### <span data-ttu-id="1ec07-112">Esempio 1: Ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="1ec07-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="1ec07-113">Questo comando recupera tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="1ec07-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="1ec07-114">Esempio 2: Ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="1ec07-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="1ec07-115">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="1ec07-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="1ec07-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec07-116">PARAMETERS</span></span>

### <span data-ttu-id="1ec07-117">-Context</span><span class="sxs-lookup"><span data-stu-id="1ec07-117">-Context</span></span>

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

### <span data-ttu-id="1ec07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec07-118">-DefaultProfile</span></span>
<span data-ttu-id="1ec07-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec07-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ec07-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ec07-120">-ResourceId</span></span>
<span data-ttu-id="1ec07-121">Arm Resource Identifier del server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="1ec07-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="1ec07-122">Se specificato, tenterà di trovare il server di autorizzazione in base all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="1ec07-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="1ec07-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ec07-123">This parameter is required.</span></span>

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

### <span data-ttu-id="1ec07-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1ec07-124">-ServerId</span></span>
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

### <span data-ttu-id="1ec07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec07-125">CommonParameters</span></span>
<span data-ttu-id="1ec07-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec07-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ec07-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec07-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1ec07-128">INPUTS</span></span>

### <span data-ttu-id="1ec07-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1ec07-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1ec07-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1ec07-130">System.String</span></span>

## <span data-ttu-id="1ec07-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ec07-131">OUTPUTS</span></span>

### <span data-ttu-id="1ec07-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ec07-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="1ec07-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="1ec07-133">NOTES</span></span>

## <span data-ttu-id="1ec07-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ec07-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ec07-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ec07-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1ec07-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ec07-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="1ec07-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="1ec07-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


