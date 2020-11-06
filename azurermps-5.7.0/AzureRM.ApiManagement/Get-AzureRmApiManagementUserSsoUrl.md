---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514579"
---
# <span data-ttu-id="bd5a4-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="bd5a4-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="bd5a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5a4-103">Genera un URL SSO per un utente.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd5a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd5a4-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd5a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="bd5a4-106">Il cmdlet **Get-AzureRmApiManagementUserSsoUrl** genera un URL Single Sign-on (SSO) per un utente.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="bd5a4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd5a4-107">EXAMPLES</span></span>

### <span data-ttu-id="bd5a4-108">Esempio 1: ottenere l'URL SSO di un utente</span><span class="sxs-lookup"><span data-stu-id="bd5a4-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="bd5a4-109">Questo comando ottiene l'URL SSO di un utente.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="bd5a4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd5a4-110">PARAMETERS</span></span>

### <span data-ttu-id="bd5a4-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bd5a4-111">-Context</span></span>
<span data-ttu-id="bd5a4-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bd5a4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bd5a4-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bd5a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd5a4-114">-DefaultProfile</span></span>
<span data-ttu-id="bd5a4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd5a4-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="bd5a4-116">-UserId</span></span>
<span data-ttu-id="bd5a4-117">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-117">Specifies a user ID.</span></span>
<span data-ttu-id="bd5a4-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5a4-119">CommonParameters</span></span>
<span data-ttu-id="bd5a4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5a4-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd5a4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5a4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd5a4-122">INPUTS</span></span>

### <span data-ttu-id="bd5a4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd5a4-123">None</span></span>
<span data-ttu-id="bd5a4-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bd5a4-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd5a4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd5a4-125">OUTPUTS</span></span>

### <span data-ttu-id="bd5a4-126">stringa</span><span class="sxs-lookup"><span data-stu-id="bd5a4-126">string</span></span>

## <span data-ttu-id="bd5a4-127">Note</span><span class="sxs-lookup"><span data-stu-id="bd5a4-127">NOTES</span></span>

## <span data-ttu-id="bd5a4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd5a4-128">RELATED LINKS</span></span>

[<span data-ttu-id="bd5a4-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bd5a4-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


