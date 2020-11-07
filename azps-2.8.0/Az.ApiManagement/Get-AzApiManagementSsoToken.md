---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676053"
---
# <span data-ttu-id="6c919-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="6c919-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="6c919-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c919-102">SYNOPSIS</span></span>
<span data-ttu-id="6c919-103">Ottiene un collegamento con un token SSO a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6c919-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="6c919-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c919-104">SYNTAX</span></span>

### <span data-ttu-id="6c919-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c919-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c919-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6c919-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c919-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c919-107">DESCRIPTION</span></span>
<span data-ttu-id="6c919-108">Il cmdlet **Get-AzApiManagementSsoToken** restituisce un collegamento (URL) che contiene un token Single Sign-on (SSO) a un portale di gestione distribuito di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6c919-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="6c919-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c919-109">EXAMPLES</span></span>

### <span data-ttu-id="6c919-110">Esempio 1: ottenere il token SSO di un servizio di gestione API</span><span class="sxs-lookup"><span data-stu-id="6c919-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="6c919-111">Questo comando ottiene il token SSO di un servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6c919-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="6c919-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c919-112">PARAMETERS</span></span>

### <span data-ttu-id="6c919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c919-113">-DefaultProfile</span></span>
<span data-ttu-id="6c919-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c919-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c919-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c919-115">-InputObject</span></span>
<span data-ttu-id="6c919-116">Istanza di PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="6c919-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="6c919-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6c919-117">This parameter is required.</span></span>

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

### <span data-ttu-id="6c919-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c919-118">-Name</span></span>
<span data-ttu-id="6c919-119">Specifica il nome dell'istanza di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6c919-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="6c919-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c919-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c919-121">Specifica il nome del gruppo di risorse in cui è presente la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="6c919-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="6c919-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c919-122">CommonParameters</span></span>
<span data-ttu-id="6c919-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c919-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c919-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c919-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c919-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c919-125">INPUTS</span></span>

### <span data-ttu-id="6c919-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6c919-126">System.String</span></span>

## <span data-ttu-id="6c919-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c919-127">OUTPUTS</span></span>

### <span data-ttu-id="6c919-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6c919-128">System.String</span></span>

## <span data-ttu-id="6c919-129">Note</span><span class="sxs-lookup"><span data-stu-id="6c919-129">NOTES</span></span>

## <span data-ttu-id="6c919-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c919-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c919-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6c919-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


