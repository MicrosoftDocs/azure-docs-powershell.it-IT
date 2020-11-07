---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673624"
---
# <span data-ttu-id="d26d4-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="d26d4-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="d26d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d26d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d26d4-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d26d4-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="d26d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d26d4-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d26d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d26d4-105">DESCRIPTION</span></span>
<span data-ttu-id="d26d4-106">Il cmdlet **Get-AzApiManagementSsoToken** restituisce un collegamento (URL) che contiene un token Single Sign-on (SSO) a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d26d4-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="d26d4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d26d4-107">EXAMPLES</span></span>

### <span data-ttu-id="d26d4-108">Esempio 1: ottenere il token SSO di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="d26d4-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="d26d4-109">Questo comando ottiene il token SSO di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d26d4-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="d26d4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d26d4-110">PARAMETERS</span></span>

### <span data-ttu-id="d26d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d26d4-111">-DefaultProfile</span></span>
<span data-ttu-id="d26d4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d26d4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d26d4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d26d4-113">-Name</span></span>
<span data-ttu-id="d26d4-114">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="d26d4-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="d26d4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d26d4-115">-ResourceGroupName</span></span>
<span data-ttu-id="d26d4-116">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="d26d4-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="d26d4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d26d4-117">CommonParameters</span></span>
<span data-ttu-id="d26d4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d26d4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d26d4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d26d4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d26d4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d26d4-120">INPUTS</span></span>

### <span data-ttu-id="d26d4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d26d4-121">System.String</span></span>

## <span data-ttu-id="d26d4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d26d4-122">OUTPUTS</span></span>

### <span data-ttu-id="d26d4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d26d4-123">System.String</span></span>

## <span data-ttu-id="d26d4-124">Note</span><span class="sxs-lookup"><span data-stu-id="d26d4-124">NOTES</span></span>

## <span data-ttu-id="d26d4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d26d4-125">RELATED LINKS</span></span>

[<span data-ttu-id="d26d4-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d26d4-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


