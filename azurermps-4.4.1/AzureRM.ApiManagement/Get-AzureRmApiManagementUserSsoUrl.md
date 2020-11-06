---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: a13d37100e553d8d56cf5b040a796adabe08b7d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517247"
---
# <span data-ttu-id="ba30d-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="ba30d-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="ba30d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba30d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba30d-103">Genera un URL SSO per un utente.</span><span class="sxs-lookup"><span data-stu-id="ba30d-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba30d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba30d-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba30d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba30d-105">DESCRIPTION</span></span>
<span data-ttu-id="ba30d-106">Il cmdlet **Get-AzureRmApiManagementUserSsoUrl** genera un URL Single Sign-on (SSO) per un utente.</span><span class="sxs-lookup"><span data-stu-id="ba30d-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="ba30d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba30d-107">EXAMPLES</span></span>

### <span data-ttu-id="ba30d-108">Esempio 1: ottenere l'URL SSO di un utente</span><span class="sxs-lookup"><span data-stu-id="ba30d-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ba30d-109">Questo comando ottiene l'URL SSO di un utente.</span><span class="sxs-lookup"><span data-stu-id="ba30d-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="ba30d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba30d-110">PARAMETERS</span></span>

### <span data-ttu-id="ba30d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ba30d-111">-Context</span></span>
<span data-ttu-id="ba30d-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ba30d-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ba30d-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba30d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ba30d-114">-UserId</span><span class="sxs-lookup"><span data-stu-id="ba30d-114">-UserId</span></span>
<span data-ttu-id="ba30d-115">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="ba30d-115">Specifies a user ID.</span></span>
<span data-ttu-id="ba30d-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba30d-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ba30d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba30d-117">-DefaultProfile</span></span>
<span data-ttu-id="ba30d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba30d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba30d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba30d-119">CommonParameters</span></span>
<span data-ttu-id="ba30d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba30d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba30d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba30d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba30d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba30d-122">INPUTS</span></span>

## <span data-ttu-id="ba30d-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba30d-123">OUTPUTS</span></span>

### <span data-ttu-id="ba30d-124">stringa</span><span class="sxs-lookup"><span data-stu-id="ba30d-124">string</span></span>

## <span data-ttu-id="ba30d-125">Note</span><span class="sxs-lookup"><span data-stu-id="ba30d-125">NOTES</span></span>

## <span data-ttu-id="ba30d-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba30d-126">RELATED LINKS</span></span>

[<span data-ttu-id="ba30d-127">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ba30d-127">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


