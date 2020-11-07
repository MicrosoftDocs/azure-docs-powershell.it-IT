---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 88147f9f26ecd31af1963c5ab378bb00262ef2ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686655"
---
# <span data-ttu-id="2ed44-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ed44-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2ed44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ed44-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed44-103">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="2ed44-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ed44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ed44-104">SYNTAX</span></span>

### <span data-ttu-id="2ed44-105">AllIdentityProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ed44-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ed44-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="2ed44-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed44-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ed44-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed44-108">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="2ed44-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="2ed44-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ed44-109">EXAMPLES</span></span>

### <span data-ttu-id="2ed44-110">Esempio 1: ottenere tutti i provider di identità</span><span class="sxs-lookup"><span data-stu-id="2ed44-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="2ed44-111">Ottenere tutta la configurazione del provider di identità nel servizio.</span><span class="sxs-lookup"><span data-stu-id="2ed44-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="2ed44-112">Ottenere il provider di identità di tipo AAD</span><span class="sxs-lookup"><span data-stu-id="2ed44-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="2ed44-113">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ed44-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="2ed44-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ed44-114">PARAMETERS</span></span>

### <span data-ttu-id="2ed44-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2ed44-115">-Context</span></span>
<span data-ttu-id="2ed44-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2ed44-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2ed44-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ed44-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2ed44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed44-118">-DefaultProfile</span></span>
<span data-ttu-id="2ed44-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed44-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="2ed44-120">-Type</span></span>
<span data-ttu-id="2ed44-121">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="2ed44-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="2ed44-122">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="2ed44-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="2ed44-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2ed44-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ed44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed44-124">CommonParameters</span></span>
<span data-ttu-id="2ed44-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed44-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed44-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ed44-127">INPUTS</span></span>

### <span data-ttu-id="2ed44-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2ed44-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2ed44-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2ed44-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="2ed44-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ed44-130">OUTPUTS</span></span>

### <span data-ttu-id="2ed44-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2ed44-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2ed44-132">Note</span><span class="sxs-lookup"><span data-stu-id="2ed44-132">NOTES</span></span>

## <span data-ttu-id="2ed44-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ed44-133">RELATED LINKS</span></span>
