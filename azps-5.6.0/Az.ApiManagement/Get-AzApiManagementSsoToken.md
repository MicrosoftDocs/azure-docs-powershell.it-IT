---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: eae199f28314db5aa50fa3247b46f02a407802fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004957"
---
# <span data-ttu-id="730f6-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="730f6-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="730f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="730f6-102">SYNOPSIS</span></span>
<span data-ttu-id="730f6-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="730f6-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="730f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="730f6-104">SYNTAX</span></span>

### <span data-ttu-id="730f6-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="730f6-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="730f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="730f6-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="730f6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="730f6-107">DESCRIPTION</span></span>
<span data-ttu-id="730f6-108">Il cmdlet **Get-AzApiManagementSsoToken** restituisce un collegamento (URL) contenente un token Single #A0 (SSO) a un portale di gestione distribuito di un servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="730f6-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="730f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="730f6-109">EXAMPLES</span></span>

### <span data-ttu-id="730f6-110">Esempio 1: Ottenere il token SSO di un servizio di gestione DELLE API</span><span class="sxs-lookup"><span data-stu-id="730f6-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="730f6-111">Questo comando ottiene il token SSO di un servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="730f6-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="730f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="730f6-112">PARAMETERS</span></span>

### <span data-ttu-id="730f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="730f6-113">-DefaultProfile</span></span>
<span data-ttu-id="730f6-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="730f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="730f6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="730f6-115">-InputObject</span></span>
<span data-ttu-id="730f6-116">Istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="730f6-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="730f6-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="730f6-117">This parameter is required.</span></span>

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

### <span data-ttu-id="730f6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="730f6-118">-Name</span></span>
<span data-ttu-id="730f6-119">Specifica il nome dell'istanza di Gestione API.</span><span class="sxs-lookup"><span data-stu-id="730f6-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="730f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="730f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="730f6-121">Specifica il nome del gruppo di risorse in cui esiste Gestione API.</span><span class="sxs-lookup"><span data-stu-id="730f6-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="730f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="730f6-122">CommonParameters</span></span>
<span data-ttu-id="730f6-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="730f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="730f6-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="730f6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="730f6-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="730f6-125">INPUTS</span></span>

### <span data-ttu-id="730f6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="730f6-126">System.String</span></span>

## <span data-ttu-id="730f6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="730f6-127">OUTPUTS</span></span>

### <span data-ttu-id="730f6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="730f6-128">System.String</span></span>

## <span data-ttu-id="730f6-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="730f6-129">NOTES</span></span>

## <span data-ttu-id="730f6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="730f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="730f6-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="730f6-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


