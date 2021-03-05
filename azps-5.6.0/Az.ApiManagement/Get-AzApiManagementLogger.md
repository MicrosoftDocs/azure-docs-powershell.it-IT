---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973006"
---
# <span data-ttu-id="15f89-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="15f89-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="15f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f89-102">SYNOPSIS</span></span>
<span data-ttu-id="15f89-103">Recupera gli oggetti Gateway di gestione API.</span><span class="sxs-lookup"><span data-stu-id="15f89-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="15f89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15f89-104">SYNTAX</span></span>

### <span data-ttu-id="15f89-105">GetAllLoggers (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15f89-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15f89-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="15f89-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15f89-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15f89-107">DESCRIPTION</span></span>
<span data-ttu-id="15f89-108">Il cmdlet **Get-AzApiManagementManagement ottiene** un **Gateway** di gestione API di Azure o tutti i logger.</span><span class="sxs-lookup"><span data-stu-id="15f89-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="15f89-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15f89-109">EXAMPLES</span></span>

### <span data-ttu-id="15f89-110">Esempio 1: Ottenere tutti i registratori</span><span class="sxs-lookup"><span data-stu-id="15f89-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="15f89-111">Questo comando recupera tutti i logger per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="15f89-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="15f89-112">Esempio 2: Ottenere un dispositivo specifico</span><span class="sxs-lookup"><span data-stu-id="15f89-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="15f89-113">Questo comando rimuove un dispositivo che ha l'ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="15f89-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="15f89-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15f89-114">PARAMETERS</span></span>

### <span data-ttu-id="15f89-115">-Context</span><span class="sxs-lookup"><span data-stu-id="15f89-115">-Context</span></span>
<span data-ttu-id="15f89-116">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="15f89-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15f89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f89-117">-DefaultProfile</span></span>
<span data-ttu-id="15f89-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15f89-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15f89-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="15f89-119">-LoggerId</span></span>
<span data-ttu-id="15f89-120">Specifica l'ID dello specifico dispositivo di registrazione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="15f89-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15f89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f89-121">CommonParameters</span></span>
<span data-ttu-id="15f89-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15f89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f89-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="15f89-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f89-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="15f89-124">INPUTS</span></span>

### <span data-ttu-id="15f89-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15f89-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15f89-126">System.String</span><span class="sxs-lookup"><span data-stu-id="15f89-126">System.String</span></span>

## <span data-ttu-id="15f89-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15f89-127">OUTPUTS</span></span>

### <span data-ttu-id="15f89-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementManagementManagement</span><span class="sxs-lookup"><span data-stu-id="15f89-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="15f89-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="15f89-129">NOTES</span></span>

## <span data-ttu-id="15f89-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15f89-130">RELATED LINKS</span></span>

[<span data-ttu-id="15f89-131">New-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="15f89-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="15f89-132">Remove-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="15f89-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="15f89-133">Set-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="15f89-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


