---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fe23034b6fc86c9aa76629f806dcb406608f456c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673642"
---
# <span data-ttu-id="00872-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="00872-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="00872-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00872-102">SYNOPSIS</span></span>
<span data-ttu-id="00872-103">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="00872-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="00872-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00872-104">SYNTAX</span></span>

### <span data-ttu-id="00872-105">AllIdentityProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00872-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00872-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="00872-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00872-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00872-107">DESCRIPTION</span></span>
<span data-ttu-id="00872-108">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="00872-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="00872-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00872-109">EXAMPLES</span></span>

### <span data-ttu-id="00872-110">Esempio 1: ottenere tutti i provider di identità</span><span class="sxs-lookup"><span data-stu-id="00872-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="00872-111">Ottenere tutta la configurazione del provider di identità nel servizio.</span><span class="sxs-lookup"><span data-stu-id="00872-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="00872-112">Ottenere il provider di identità di tipo AAD</span><span class="sxs-lookup"><span data-stu-id="00872-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="00872-113">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00872-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="00872-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00872-114">PARAMETERS</span></span>

### <span data-ttu-id="00872-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="00872-115">-Context</span></span>
<span data-ttu-id="00872-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="00872-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="00872-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="00872-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00872-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00872-118">-DefaultProfile</span></span>
<span data-ttu-id="00872-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00872-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00872-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="00872-120">-Type</span></span>
<span data-ttu-id="00872-121">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="00872-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="00872-122">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="00872-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="00872-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="00872-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00872-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00872-124">CommonParameters</span></span>
<span data-ttu-id="00872-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00872-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00872-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00872-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00872-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00872-127">INPUTS</span></span>

### <span data-ttu-id="00872-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00872-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00872-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="00872-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="00872-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00872-130">OUTPUTS</span></span>

### <span data-ttu-id="00872-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="00872-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="00872-132">Note</span><span class="sxs-lookup"><span data-stu-id="00872-132">NOTES</span></span>

## <span data-ttu-id="00872-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00872-133">RELATED LINKS</span></span>
