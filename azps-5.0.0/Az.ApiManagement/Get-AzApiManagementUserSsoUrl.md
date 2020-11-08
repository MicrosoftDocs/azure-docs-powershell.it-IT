---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199923"
---
# <span data-ttu-id="396ca-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="396ca-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="396ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="396ca-102">SYNOPSIS</span></span>
<span data-ttu-id="396ca-103">Genera un URL SSO per un utente.</span><span class="sxs-lookup"><span data-stu-id="396ca-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="396ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="396ca-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="396ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="396ca-105">DESCRIPTION</span></span>
<span data-ttu-id="396ca-106">Il cmdlet **Get-AzApiManagementUserSsoUrl** genera un URL Single Sign-on (SSO) per un utente.</span><span class="sxs-lookup"><span data-stu-id="396ca-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="396ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="396ca-107">EXAMPLES</span></span>

### <span data-ttu-id="396ca-108">Esempio 1: ottenere l'URL SSO di un utente</span><span class="sxs-lookup"><span data-stu-id="396ca-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="396ca-109">Questo comando ottiene l'URL SSO di un utente.</span><span class="sxs-lookup"><span data-stu-id="396ca-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="396ca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="396ca-110">PARAMETERS</span></span>

### <span data-ttu-id="396ca-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="396ca-111">-Context</span></span>
<span data-ttu-id="396ca-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="396ca-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="396ca-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="396ca-113">This parameter is required.</span></span>

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

### <span data-ttu-id="396ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396ca-114">-DefaultProfile</span></span>
<span data-ttu-id="396ca-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="396ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="396ca-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="396ca-116">-UserId</span></span>
<span data-ttu-id="396ca-117">Specifica un ID utente.</span><span class="sxs-lookup"><span data-stu-id="396ca-117">Specifies a user ID.</span></span>
<span data-ttu-id="396ca-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="396ca-118">This parameter is required.</span></span>

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

### <span data-ttu-id="396ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396ca-119">CommonParameters</span></span>
<span data-ttu-id="396ca-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396ca-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="396ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396ca-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="396ca-122">INPUTS</span></span>

### <span data-ttu-id="396ca-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="396ca-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="396ca-124">System. String</span><span class="sxs-lookup"><span data-stu-id="396ca-124">System.String</span></span>

## <span data-ttu-id="396ca-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="396ca-125">OUTPUTS</span></span>

### <span data-ttu-id="396ca-126">System. String</span><span class="sxs-lookup"><span data-stu-id="396ca-126">System.String</span></span>

## <span data-ttu-id="396ca-127">Note</span><span class="sxs-lookup"><span data-stu-id="396ca-127">NOTES</span></span>

## <span data-ttu-id="396ca-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="396ca-128">RELATED LINKS</span></span>

[<span data-ttu-id="396ca-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="396ca-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


