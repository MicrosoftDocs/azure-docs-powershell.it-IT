---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199745"
---
# <span data-ttu-id="17466-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="17466-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="17466-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17466-102">SYNOPSIS</span></span>
<span data-ttu-id="17466-103">Ottiene gli oggetti logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="17466-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="17466-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17466-104">SYNTAX</span></span>

### <span data-ttu-id="17466-105">GetAllLoggers (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17466-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17466-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="17466-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17466-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17466-107">DESCRIPTION</span></span>
<span data-ttu-id="17466-108">Il cmdlet **Get-AzApiManagementLogger** ottiene un **logger** di gestione delle API di Azure o tutti i logger.</span><span class="sxs-lookup"><span data-stu-id="17466-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="17466-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17466-109">EXAMPLES</span></span>

### <span data-ttu-id="17466-110">Esempio 1: ottenere tutti i logger</span><span class="sxs-lookup"><span data-stu-id="17466-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="17466-111">Questo comando ottiene tutti i logger per il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="17466-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="17466-112">Esempio 2: ottenere un logger specifico</span><span class="sxs-lookup"><span data-stu-id="17466-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="17466-113">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="17466-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="17466-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17466-114">PARAMETERS</span></span>

### <span data-ttu-id="17466-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="17466-115">-Context</span></span>
<span data-ttu-id="17466-116">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="17466-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="17466-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17466-117">-DefaultProfile</span></span>
<span data-ttu-id="17466-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17466-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17466-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="17466-119">-LoggerId</span></span>
<span data-ttu-id="17466-120">Specifica l'ID del logger specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="17466-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="17466-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17466-121">CommonParameters</span></span>
<span data-ttu-id="17466-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17466-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17466-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17466-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17466-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17466-124">INPUTS</span></span>

### <span data-ttu-id="17466-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17466-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17466-126">System. String</span><span class="sxs-lookup"><span data-stu-id="17466-126">System.String</span></span>

## <span data-ttu-id="17466-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17466-127">OUTPUTS</span></span>

### <span data-ttu-id="17466-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="17466-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="17466-129">Note</span><span class="sxs-lookup"><span data-stu-id="17466-129">NOTES</span></span>

## <span data-ttu-id="17466-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17466-130">RELATED LINKS</span></span>

[<span data-ttu-id="17466-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="17466-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="17466-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="17466-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="17466-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="17466-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


