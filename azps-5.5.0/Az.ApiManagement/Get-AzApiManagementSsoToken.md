---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176510"
---
# <span data-ttu-id="ba7eb-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="ba7eb-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="ba7eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7eb-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="ba7eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-104">SYNTAX</span></span>

### <span data-ttu-id="ba7eb-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba7eb-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7eb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba7eb-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7eb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba7eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ba7eb-108">Il cmdlet **Get-AzApiManagementSsoToken** restituisce un collegamento (URL) contenente un token Single #A0 (SSO) a un portale di gestione distribuito di un servizio di gestione DELLE API.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="ba7eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ba7eb-110">Esempio 1: Ottenere il token SSO di un servizio di gestione DELLE API</span><span class="sxs-lookup"><span data-stu-id="ba7eb-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="ba7eb-111">Questo comando ottiene il token SSO di un servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="ba7eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba7eb-112">PARAMETERS</span></span>

### <span data-ttu-id="ba7eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7eb-113">-DefaultProfile</span></span>
<span data-ttu-id="ba7eb-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba7eb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba7eb-115">-InputObject</span></span>
<span data-ttu-id="ba7eb-116">Istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="ba7eb-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ba7eb-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ba7eb-118">-Name</span></span>
<span data-ttu-id="ba7eb-119">Specifica il nome dell'istanza di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="ba7eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="ba7eb-121">Specifica il nome del gruppo di risorse in cui esiste Gestione API.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="ba7eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7eb-122">CommonParameters</span></span>
<span data-ttu-id="ba7eb-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7eb-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7eb-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba7eb-125">INPUTS</span></span>

### <span data-ttu-id="ba7eb-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ba7eb-126">System.String</span></span>

## <span data-ttu-id="ba7eb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba7eb-127">OUTPUTS</span></span>

### <span data-ttu-id="ba7eb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ba7eb-128">System.String</span></span>

## <span data-ttu-id="ba7eb-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba7eb-129">NOTES</span></span>

## <span data-ttu-id="ba7eb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba7eb-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ba7eb-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


