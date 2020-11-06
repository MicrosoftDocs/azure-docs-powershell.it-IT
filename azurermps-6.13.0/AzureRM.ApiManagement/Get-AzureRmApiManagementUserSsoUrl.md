---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517696"
---
# <span data-ttu-id="bce16-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="bce16-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="bce16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bce16-102">SYNOPSIS</span></span>
<span data-ttu-id="bce16-103">Genera un URL SSO per un utente.</span><span class="sxs-lookup"><span data-stu-id="bce16-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bce16-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bce16-105">DESCRIPTION</span></span>
<span data-ttu-id="bce16-106">Il cmdlet **Get-AzureRmApiManagementUserSsoUrl** genera un URL Single Sign-on (SSO) per un utente.</span><span class="sxs-lookup"><span data-stu-id="bce16-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="bce16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bce16-107">EXAMPLES</span></span>

### <span data-ttu-id="bce16-108">Esempio 1: ottenere l'URL SSO di un utente</span><span class="sxs-lookup"><span data-stu-id="bce16-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="bce16-109">Questo comando ottiene l'URL SSO di un utente.</span><span class="sxs-lookup"><span data-stu-id="bce16-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="bce16-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bce16-110">PARAMETERS</span></span>

### <span data-ttu-id="bce16-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bce16-111">-Context</span></span>
<span data-ttu-id="bce16-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bce16-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="bce16-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bce16-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bce16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce16-114">-DefaultProfile</span></span>
<span data-ttu-id="bce16-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bce16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce16-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="bce16-116">-UserId</span></span>
<span data-ttu-id="bce16-117">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="bce16-117">Specifies a user ID.</span></span>
<span data-ttu-id="bce16-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="bce16-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce16-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce16-119">CommonParameters</span></span>
<span data-ttu-id="bce16-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce16-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce16-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce16-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce16-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bce16-122">INPUTS</span></span>

### <span data-ttu-id="bce16-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bce16-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bce16-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bce16-124">System.String</span></span>

## <span data-ttu-id="bce16-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bce16-125">OUTPUTS</span></span>

### <span data-ttu-id="bce16-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bce16-126">System.String</span></span>

## <span data-ttu-id="bce16-127">Note</span><span class="sxs-lookup"><span data-stu-id="bce16-127">NOTES</span></span>

## <span data-ttu-id="bce16-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bce16-128">RELATED LINKS</span></span>

[<span data-ttu-id="bce16-129">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="bce16-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


