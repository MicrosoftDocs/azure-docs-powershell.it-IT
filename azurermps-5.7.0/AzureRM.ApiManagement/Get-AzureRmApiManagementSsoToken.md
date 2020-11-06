---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514596"
---
# <span data-ttu-id="caca5-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="caca5-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="caca5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="caca5-102">SYNOPSIS</span></span>
<span data-ttu-id="caca5-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="caca5-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="caca5-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caca5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="caca5-105">DESCRIPTION</span></span>
<span data-ttu-id="caca5-106">Il cmdlet **Get-AzureRmApiManagementSsoToken** restituisce un collegamento (URL) che contiene un token Single Sign-on (SSO) a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="caca5-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="caca5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="caca5-107">EXAMPLES</span></span>

### <span data-ttu-id="caca5-108">Esempio 1: ottenere il token SSO di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="caca5-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="caca5-109">Questo comando ottiene il token SSO di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="caca5-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="caca5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="caca5-110">PARAMETERS</span></span>

### <span data-ttu-id="caca5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caca5-111">-DefaultProfile</span></span>
<span data-ttu-id="caca5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="caca5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="caca5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="caca5-113">-Name</span></span>
<span data-ttu-id="caca5-114">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="caca5-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="caca5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caca5-115">-ResourceGroupName</span></span>
<span data-ttu-id="caca5-116">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="caca5-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="caca5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caca5-117">CommonParameters</span></span>
<span data-ttu-id="caca5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caca5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caca5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caca5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caca5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="caca5-120">INPUTS</span></span>

### <span data-ttu-id="caca5-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="caca5-121">None</span></span>
<span data-ttu-id="caca5-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="caca5-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="caca5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="caca5-123">OUTPUTS</span></span>

### <span data-ttu-id="caca5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="caca5-124">System.String</span></span>

## <span data-ttu-id="caca5-125">Note</span><span class="sxs-lookup"><span data-stu-id="caca5-125">NOTES</span></span>

## <span data-ttu-id="caca5-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="caca5-126">RELATED LINKS</span></span>

[<span data-ttu-id="caca5-127">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="caca5-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


