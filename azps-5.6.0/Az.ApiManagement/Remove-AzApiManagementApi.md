---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: d1ef516fc8b95814685350eb309e0a56d08d4b59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959117"
---
# <span data-ttu-id="85582-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="85582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85582-102">SYNOPSIS</span></span>
<span data-ttu-id="85582-103">Rimuove un'API.</span><span class="sxs-lookup"><span data-stu-id="85582-103">Removes an API.</span></span>

## <span data-ttu-id="85582-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85582-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85582-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85582-105">DESCRIPTION</span></span>
<span data-ttu-id="85582-106">Il cmdlet **Remove-AzApiManagementApi** rimuove un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="85582-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="85582-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85582-107">EXAMPLES</span></span>

### <span data-ttu-id="85582-108">Esempio 1: Rimuovere un'API</span><span class="sxs-lookup"><span data-stu-id="85582-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="85582-109">Questo comando rimuove l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="85582-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="85582-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85582-110">PARAMETERS</span></span>

### <span data-ttu-id="85582-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="85582-111">-ApiId</span></span>
<span data-ttu-id="85582-112">Specifica l'ID della rimozione dell'API.</span><span class="sxs-lookup"><span data-stu-id="85582-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="85582-113">-Context</span><span class="sxs-lookup"><span data-stu-id="85582-113">-Context</span></span>
<span data-ttu-id="85582-114">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="85582-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="85582-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85582-115">-DefaultProfile</span></span>
<span data-ttu-id="85582-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85582-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85582-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85582-117">-PassThru</span></span>
<span data-ttu-id="85582-118">passthru</span><span class="sxs-lookup"><span data-stu-id="85582-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85582-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85582-119">-Confirm</span></span>
<span data-ttu-id="85582-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85582-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85582-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85582-121">-WhatIf</span></span>
<span data-ttu-id="85582-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85582-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85582-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85582-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85582-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85582-124">CommonParameters</span></span>
<span data-ttu-id="85582-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85582-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85582-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85582-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85582-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="85582-127">INPUTS</span></span>

### <span data-ttu-id="85582-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="85582-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="85582-129">System.String</span><span class="sxs-lookup"><span data-stu-id="85582-129">System.String</span></span>

### <span data-ttu-id="85582-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="85582-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="85582-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85582-131">OUTPUTS</span></span>

### <span data-ttu-id="85582-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85582-132">System.Boolean</span></span>

## <span data-ttu-id="85582-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="85582-133">NOTES</span></span>

## <span data-ttu-id="85582-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85582-134">RELATED LINKS</span></span>

[<span data-ttu-id="85582-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="85582-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="85582-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="85582-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="85582-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="85582-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


