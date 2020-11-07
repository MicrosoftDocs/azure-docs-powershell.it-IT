---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 7ca683fc8b4c84a31a651982e5b605d3c29123a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685540"
---
# <span data-ttu-id="345dd-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="345dd-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="345dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="345dd-102">SYNOPSIS</span></span>
<span data-ttu-id="345dd-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="345dd-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="345dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="345dd-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="345dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="345dd-105">DESCRIPTION</span></span>
<span data-ttu-id="345dd-106">Il cmdlet **Get-AzureRmApiManagementSsoToken** restituisce un collegamento (URL) che contiene un token Single Sign-on (SSO) a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="345dd-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="345dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="345dd-107">EXAMPLES</span></span>

### <span data-ttu-id="345dd-108">Esempio 1: ottenere il token SSO di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="345dd-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="345dd-109">Questo comando ottiene il token SSO di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="345dd-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="345dd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="345dd-110">PARAMETERS</span></span>

### <span data-ttu-id="345dd-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="345dd-111">-Name</span></span>
<span data-ttu-id="345dd-112">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="345dd-112">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="345dd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="345dd-113">-ResourceGroupName</span></span>
<span data-ttu-id="345dd-114">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="345dd-114">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="345dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="345dd-115">-DefaultProfile</span></span>
<span data-ttu-id="345dd-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="345dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="345dd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="345dd-117">CommonParameters</span></span>
<span data-ttu-id="345dd-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="345dd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="345dd-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="345dd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="345dd-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="345dd-120">INPUTS</span></span>

## <span data-ttu-id="345dd-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="345dd-121">OUTPUTS</span></span>

### <span data-ttu-id="345dd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="345dd-122">System.String</span></span>

## <span data-ttu-id="345dd-123">Note</span><span class="sxs-lookup"><span data-stu-id="345dd-123">NOTES</span></span>

## <span data-ttu-id="345dd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="345dd-124">RELATED LINKS</span></span>

[<span data-ttu-id="345dd-125">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="345dd-125">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


