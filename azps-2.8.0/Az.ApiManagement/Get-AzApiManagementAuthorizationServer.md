---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676080"
---
# <span data-ttu-id="52d6a-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="52d6a-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="52d6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="52d6a-103">Ottiene un server di autorizzazione Gestione API.</span><span class="sxs-lookup"><span data-stu-id="52d6a-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="52d6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52d6a-104">SYNTAX</span></span>

### <span data-ttu-id="52d6a-105">ContextParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52d6a-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52d6a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52d6a-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d6a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="52d6a-108">Il cmdlet **Get-AzApiManagementAuthorizationServer** ottiene tutti i server di autorizzazione di gestione delle API Azure o i server di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="52d6a-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="52d6a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52d6a-109">EXAMPLES</span></span>

### <span data-ttu-id="52d6a-110">Esempio 1: ottenere tutti i server di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="52d6a-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="52d6a-111">Questo comando ottiene tutti i server di autorizzazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="52d6a-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="52d6a-112">Esempio 2: ottenere un server di autorizzazione specificato</span><span class="sxs-lookup"><span data-stu-id="52d6a-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="52d6a-113">Questo comando ottiene il server di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="52d6a-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="52d6a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52d6a-114">PARAMETERS</span></span>

### <span data-ttu-id="52d6a-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="52d6a-115">-Context</span></span>

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

### <span data-ttu-id="52d6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d6a-116">-DefaultProfile</span></span>
<span data-ttu-id="52d6a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52d6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d6a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52d6a-118">-ResourceId</span></span>
<span data-ttu-id="52d6a-119">Identificatore delle risorse ARM del server di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="52d6a-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="52d6a-120">Se specificato cercherà di trovare il server di autorizzazione dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="52d6a-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="52d6a-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="52d6a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="52d6a-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="52d6a-122">-ServerId</span></span>
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

### <span data-ttu-id="52d6a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d6a-123">CommonParameters</span></span>
<span data-ttu-id="52d6a-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d6a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d6a-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52d6a-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d6a-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52d6a-126">INPUTS</span></span>

### <span data-ttu-id="52d6a-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52d6a-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52d6a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="52d6a-128">System.String</span></span>

## <span data-ttu-id="52d6a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52d6a-129">OUTPUTS</span></span>

### <span data-ttu-id="52d6a-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="52d6a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="52d6a-131">Note</span><span class="sxs-lookup"><span data-stu-id="52d6a-131">NOTES</span></span>

## <span data-ttu-id="52d6a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52d6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="52d6a-133">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="52d6a-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="52d6a-134">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="52d6a-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="52d6a-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="52d6a-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


