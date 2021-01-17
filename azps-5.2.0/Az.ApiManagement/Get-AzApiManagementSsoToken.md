---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360541"
---
# <span data-ttu-id="2da39-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="2da39-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="2da39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2da39-102">SYNOPSIS</span></span>
<span data-ttu-id="2da39-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="2da39-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="2da39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2da39-104">SYNTAX</span></span>

### <span data-ttu-id="2da39-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2da39-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2da39-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2da39-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2da39-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2da39-107">DESCRIPTION</span></span>
<span data-ttu-id="2da39-108">Il cmdlet **Get-AzApiManagementSsoToken** restituisce un collegamento (URL) che contiene un token Single Sign-on (SSO) a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="2da39-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="2da39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2da39-109">EXAMPLES</span></span>

### <span data-ttu-id="2da39-110">Esempio 1: ottenere il token SSO di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="2da39-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="2da39-111">Questo comando ottiene il token SSO di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="2da39-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="2da39-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2da39-112">PARAMETERS</span></span>

### <span data-ttu-id="2da39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da39-113">-DefaultProfile</span></span>
<span data-ttu-id="2da39-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2da39-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2da39-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2da39-115">-InputObject</span></span>
<span data-ttu-id="2da39-116">Istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2da39-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="2da39-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2da39-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2da39-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2da39-118">-Name</span></span>
<span data-ttu-id="2da39-119">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="2da39-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da39-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2da39-120">-ResourceGroupName</span></span>
<span data-ttu-id="2da39-121">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="2da39-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2da39-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da39-122">CommonParameters</span></span>
<span data-ttu-id="2da39-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da39-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da39-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2da39-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da39-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2da39-125">INPUTS</span></span>

### <span data-ttu-id="2da39-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2da39-126">System.String</span></span>

## <span data-ttu-id="2da39-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2da39-127">OUTPUTS</span></span>

### <span data-ttu-id="2da39-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2da39-128">System.String</span></span>

## <span data-ttu-id="2da39-129">Note</span><span class="sxs-lookup"><span data-stu-id="2da39-129">NOTES</span></span>

## <span data-ttu-id="2da39-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2da39-130">RELATED LINKS</span></span>

[<span data-ttu-id="2da39-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2da39-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


