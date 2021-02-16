---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176495"
---
# <span data-ttu-id="c7309-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="c7309-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="c7309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7309-102">SYNOPSIS</span></span>
<span data-ttu-id="c7309-103">Genera un URL SSO per un utente.</span><span class="sxs-lookup"><span data-stu-id="c7309-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="c7309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7309-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7309-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7309-105">DESCRIPTION</span></span>
<span data-ttu-id="c7309-106">Il cmdlet **Get-AzApiManagementUserSsoUrl** genera un URL Single #A0 (SSO) per un utente.</span><span class="sxs-lookup"><span data-stu-id="c7309-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="c7309-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7309-107">EXAMPLES</span></span>

### <span data-ttu-id="c7309-108">Esempio 1: Ottenere l'URL SSO di un utente</span><span class="sxs-lookup"><span data-stu-id="c7309-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="c7309-109">Questo comando ottiene l'URL SSO di un utente.</span><span class="sxs-lookup"><span data-stu-id="c7309-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="c7309-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7309-110">PARAMETERS</span></span>

### <span data-ttu-id="c7309-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c7309-111">-Context</span></span>
<span data-ttu-id="c7309-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c7309-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c7309-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7309-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7309-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7309-114">-DefaultProfile</span></span>
<span data-ttu-id="c7309-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7309-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7309-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="c7309-116">-UserId</span></span>
<span data-ttu-id="c7309-117">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="c7309-117">Specifies a user ID.</span></span>
<span data-ttu-id="c7309-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7309-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c7309-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7309-119">CommonParameters</span></span>
<span data-ttu-id="c7309-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7309-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7309-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7309-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7309-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7309-122">INPUTS</span></span>

### <span data-ttu-id="c7309-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7309-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7309-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c7309-124">System.String</span></span>

## <span data-ttu-id="c7309-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7309-125">OUTPUTS</span></span>

### <span data-ttu-id="c7309-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c7309-126">System.String</span></span>

## <span data-ttu-id="c7309-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7309-127">NOTES</span></span>

## <span data-ttu-id="c7309-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7309-128">RELATED LINKS</span></span>

[<span data-ttu-id="c7309-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="c7309-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


