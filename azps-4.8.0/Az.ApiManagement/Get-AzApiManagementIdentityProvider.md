---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033358"
---
# <span data-ttu-id="33a3a-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="33a3a-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="33a3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="33a3a-103">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="33a3a-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="33a3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33a3a-104">SYNTAX</span></span>

### <span data-ttu-id="33a3a-105">AllIdentityProviders (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33a3a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33a3a-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="33a3a-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33a3a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33a3a-107">DESCRIPTION</span></span>
<span data-ttu-id="33a3a-108">Ottenere i dettagli della configurazione del provider di identità.</span><span class="sxs-lookup"><span data-stu-id="33a3a-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="33a3a-109">ClientSecret non verrà incluso nei dettagli dei risultati.</span><span class="sxs-lookup"><span data-stu-id="33a3a-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="33a3a-110">Per ottenere il segreto del client, USA **Get-AzApiManagementIdentityProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="33a3a-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="33a3a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33a3a-111">EXAMPLES</span></span>

### <span data-ttu-id="33a3a-112">Esempio 1: ottenere tutti i provider di identità</span><span class="sxs-lookup"><span data-stu-id="33a3a-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="33a3a-113">Ottenere tutta la configurazione del provider di identità nel servizio.</span><span class="sxs-lookup"><span data-stu-id="33a3a-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="33a3a-114">Esempio 2: ottenere il provider di identità di tipo AAD</span><span class="sxs-lookup"><span data-stu-id="33a3a-114">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="33a3a-115">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33a3a-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="33a3a-116">Esempio 3: ottenere il provider di identità di tipo AAD B2C</span><span class="sxs-lookup"><span data-stu-id="33a3a-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="33a3a-117">Ottiene la configurazione del provider di identità di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33a3a-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="33a3a-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33a3a-118">PARAMETERS</span></span>

### <span data-ttu-id="33a3a-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="33a3a-119">-Context</span></span>
<span data-ttu-id="33a3a-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="33a3a-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="33a3a-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="33a3a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="33a3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a3a-122">-DefaultProfile</span></span>
<span data-ttu-id="33a3a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33a3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a3a-124">-Digitare</span><span class="sxs-lookup"><span data-stu-id="33a3a-124">-Type</span></span>
<span data-ttu-id="33a3a-125">Identificatore di un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="33a3a-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="33a3a-126">Se specificato cercherà di trovare la configurazione del provider di identità dall'identificatore.</span><span class="sxs-lookup"><span data-stu-id="33a3a-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="33a3a-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="33a3a-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="33a3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a3a-128">CommonParameters</span></span>
<span data-ttu-id="33a3a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a3a-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33a3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a3a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33a3a-131">INPUTS</span></span>

### <span data-ttu-id="33a3a-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33a3a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33a3a-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="33a3a-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="33a3a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33a3a-134">OUTPUTS</span></span>

### <span data-ttu-id="33a3a-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="33a3a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="33a3a-136">Note</span><span class="sxs-lookup"><span data-stu-id="33a3a-136">NOTES</span></span>

## <span data-ttu-id="33a3a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33a3a-137">RELATED LINKS</span></span>
