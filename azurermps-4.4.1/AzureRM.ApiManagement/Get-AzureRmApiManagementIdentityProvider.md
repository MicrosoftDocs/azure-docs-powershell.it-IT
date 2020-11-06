---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517267"
---
# <span data-ttu-id="c654b-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c654b-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c654b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c654b-102">SYNOPSIS</span></span>
<span data-ttu-id="c654b-103">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="c654b-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c654b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c654b-104">SYNTAX</span></span>

### <span data-ttu-id="c654b-105">AllIdentityProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c654b-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c654b-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="c654b-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c654b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c654b-107">DESCRIPTION</span></span>
<span data-ttu-id="c654b-108">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="c654b-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="c654b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c654b-109">EXAMPLES</span></span>

### <span data-ttu-id="c654b-110">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c654b-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="c654b-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c654b-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="c654b-112">Ottenere tutta la configurazione del provider di identità nel servizio.</span><span class="sxs-lookup"><span data-stu-id="c654b-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="c654b-113">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c654b-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="c654b-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="c654b-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="c654b-115">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c654b-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="c654b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c654b-116">PARAMETERS</span></span>

### <span data-ttu-id="c654b-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c654b-117">-Context</span></span>
<span data-ttu-id="c654b-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c654b-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c654b-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c654b-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c654b-120">-Digitare</span><span class="sxs-lookup"><span data-stu-id="c654b-120">-Type</span></span>
<span data-ttu-id="c654b-121">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="c654b-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="c654b-122">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="c654b-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="c654b-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654b-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c654b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c654b-124">-DefaultProfile</span></span>
<span data-ttu-id="c654b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c654b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c654b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c654b-126">CommonParameters</span></span>
<span data-ttu-id="c654b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c654b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c654b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c654b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c654b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c654b-129">INPUTS</span></span>

## <span data-ttu-id="c654b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c654b-130">OUTPUTS</span></span>

### <span data-ttu-id="c654b-131">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="c654b-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="c654b-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c654b-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c654b-133">Note</span><span class="sxs-lookup"><span data-stu-id="c654b-133">NOTES</span></span>

## <span data-ttu-id="c654b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c654b-134">RELATED LINKS</span></span>

