---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302251"
---
# <span data-ttu-id="04667-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04667-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="04667-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04667-102">SYNOPSIS</span></span>
<span data-ttu-id="04667-103">Ottiene un server di autorizzazione Gestione API.</span><span class="sxs-lookup"><span data-stu-id="04667-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="04667-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04667-104">SYNTAX</span></span>

### <span data-ttu-id="04667-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04667-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04667-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04667-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04667-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04667-107">DESCRIPTION</span></span>
<span data-ttu-id="04667-108">Il cmdlet **Get-AzApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione di gestione delle API Azure o il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="04667-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="04667-109">ClientSecret non verrà incluso nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="04667-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="04667-110">Per ottenere il segreto del client, USA **Get-AzApiManagementAuthorizationServerClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="04667-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="04667-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04667-111">EXAMPLES</span></span>

### <span data-ttu-id="04667-112">Esempio 1: ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="04667-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="04667-113">Questo comando ottiene tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="04667-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="04667-114">Esempio 2: ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="04667-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="04667-115">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="04667-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="04667-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04667-116">PARAMETERS</span></span>

### <span data-ttu-id="04667-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="04667-117">-Context</span></span>

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

### <span data-ttu-id="04667-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04667-118">-DefaultProfile</span></span>
<span data-ttu-id="04667-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04667-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04667-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04667-120">-ResourceId</span></span>
<span data-ttu-id="04667-121">Identificatore delle risorse ARM del server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="04667-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="04667-122">Se specificato cercherà di trovare il server di autorizzazione dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="04667-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="04667-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="04667-123">This parameter is required.</span></span>

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

### <span data-ttu-id="04667-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="04667-124">-ServerId</span></span>
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

### <span data-ttu-id="04667-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04667-125">CommonParameters</span></span>
<span data-ttu-id="04667-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04667-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04667-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04667-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04667-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04667-128">INPUTS</span></span>

### <span data-ttu-id="04667-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04667-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04667-130">System. String</span><span class="sxs-lookup"><span data-stu-id="04667-130">System.String</span></span>

## <span data-ttu-id="04667-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04667-131">OUTPUTS</span></span>

### <span data-ttu-id="04667-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04667-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="04667-133">Note</span><span class="sxs-lookup"><span data-stu-id="04667-133">NOTES</span></span>

## <span data-ttu-id="04667-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04667-134">RELATED LINKS</span></span>

[<span data-ttu-id="04667-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04667-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="04667-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04667-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="04667-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="04667-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


