---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199727"
---
# <span data-ttu-id="d4616-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="d4616-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="d4616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4616-102">SYNOPSIS</span></span>
<span data-ttu-id="d4616-103">Rimuove un valore denominato gestione API.</span><span class="sxs-lookup"><span data-stu-id="d4616-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="d4616-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4616-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4616-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4616-105">DESCRIPTION</span></span>
<span data-ttu-id="d4616-106">Il cmdlet **Remove-AzApiManagementNamedValue** rimuove un valore denominato Gestione API **di** Azure.</span><span class="sxs-lookup"><span data-stu-id="d4616-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="d4616-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4616-107">EXAMPLES</span></span>

### <span data-ttu-id="d4616-108">Esempio 1: Rimuovere il valore denominato</span><span class="sxs-lookup"><span data-stu-id="d4616-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="d4616-109">Questo comando rimuove il valore denominato con ID Property11.</span><span class="sxs-lookup"><span data-stu-id="d4616-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="d4616-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4616-110">PARAMETERS</span></span>

### <span data-ttu-id="d4616-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d4616-111">-Context</span></span>
<span data-ttu-id="d4616-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4616-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d4616-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4616-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d4616-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4616-114">-DefaultProfile</span></span>
<span data-ttu-id="d4616-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4616-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4616-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="d4616-116">-NamedValueId</span></span>
<span data-ttu-id="d4616-117">Identificatore di un valore denominato esistente.</span><span class="sxs-lookup"><span data-stu-id="d4616-117">Identifier of existing named value.</span></span>
<span data-ttu-id="d4616-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="d4616-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d4616-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4616-119">-PassThru</span></span>
<span data-ttu-id="d4616-120">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="d4616-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d4616-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d4616-121">This parameter is optional.</span></span>
<span data-ttu-id="d4616-122">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="d4616-122">Default value is false.</span></span>

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

### <span data-ttu-id="d4616-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4616-123">-Confirm</span></span>
<span data-ttu-id="d4616-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4616-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4616-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4616-125">-WhatIf</span></span>
<span data-ttu-id="d4616-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4616-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4616-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4616-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4616-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4616-128">CommonParameters</span></span>
<span data-ttu-id="d4616-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4616-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4616-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4616-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4616-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4616-131">INPUTS</span></span>

### <span data-ttu-id="d4616-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4616-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d4616-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d4616-133">System.String</span></span>

### <span data-ttu-id="d4616-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4616-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4616-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4616-135">OUTPUTS</span></span>

### <span data-ttu-id="d4616-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4616-136">System.Boolean</span></span>

## <span data-ttu-id="d4616-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4616-137">NOTES</span></span>

## <span data-ttu-id="d4616-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4616-138">RELATED LINKS</span></span>
