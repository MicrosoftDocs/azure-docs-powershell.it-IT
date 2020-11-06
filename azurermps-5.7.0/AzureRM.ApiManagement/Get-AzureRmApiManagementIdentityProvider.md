---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519477"
---
# <span data-ttu-id="0bee4-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bee4-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0bee4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bee4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bee4-103">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="0bee4-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bee4-104">SYNTAX</span></span>

### <span data-ttu-id="0bee4-105">AllIdentityProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0bee4-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bee4-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="0bee4-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bee4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bee4-107">DESCRIPTION</span></span>
<span data-ttu-id="0bee4-108">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="0bee4-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="0bee4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bee4-109">EXAMPLES</span></span>

### <span data-ttu-id="0bee4-110">Esempio 1: ottenere tutti i provider di identità</span><span class="sxs-lookup"><span data-stu-id="0bee4-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="0bee4-111">Ottenere tutta la configurazione del provider di identità nel servizio.</span><span class="sxs-lookup"><span data-stu-id="0bee4-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="0bee4-112">Ottenere il provider di identità di tipo AAD</span><span class="sxs-lookup"><span data-stu-id="0bee4-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="0bee4-113">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0bee4-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="0bee4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bee4-114">PARAMETERS</span></span>

### <span data-ttu-id="0bee4-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0bee4-115">-Context</span></span>
<span data-ttu-id="0bee4-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0bee4-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0bee4-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0bee4-117">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bee4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bee4-118">-DefaultProfile</span></span>
<span data-ttu-id="0bee4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bee4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bee4-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="0bee4-120">-Type</span></span>
<span data-ttu-id="0bee4-121">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="0bee4-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0bee4-122">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="0bee4-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0bee4-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0bee4-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bee4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bee4-124">CommonParameters</span></span>
<span data-ttu-id="0bee4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bee4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bee4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bee4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bee4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bee4-127">INPUTS</span></span>

### <span data-ttu-id="0bee4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0bee4-128">None</span></span>
<span data-ttu-id="0bee4-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0bee4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0bee4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bee4-130">OUTPUTS</span></span>

### <span data-ttu-id="0bee4-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bee4-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="0bee4-132">Dettagli del provider di identità configurato nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="0bee4-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="0bee4-133">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="0bee4-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="0bee4-134">Elenco dei provider di identità configurati nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="0bee4-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="0bee4-135">Note</span><span class="sxs-lookup"><span data-stu-id="0bee4-135">NOTES</span></span>

## <span data-ttu-id="0bee4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bee4-136">RELATED LINKS</span></span>

