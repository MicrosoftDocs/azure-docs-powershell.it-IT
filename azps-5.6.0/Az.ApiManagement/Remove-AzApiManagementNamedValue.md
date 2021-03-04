---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957822"
---
# <span data-ttu-id="080f0-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="080f0-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="080f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="080f0-102">SYNOPSIS</span></span>
<span data-ttu-id="080f0-103">Rimuove un valore denominato gestione API.</span><span class="sxs-lookup"><span data-stu-id="080f0-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="080f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="080f0-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="080f0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="080f0-105">DESCRIPTION</span></span>
<span data-ttu-id="080f0-106">Il cmdlet **Remove-AzApiManagementNamedValue** rimuove un valore denominato Gestione API **di** Azure.</span><span class="sxs-lookup"><span data-stu-id="080f0-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="080f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="080f0-107">EXAMPLES</span></span>

### <span data-ttu-id="080f0-108">Esempio 1: Rimuovere il valore denominato</span><span class="sxs-lookup"><span data-stu-id="080f0-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="080f0-109">Questo comando rimuove il valore denominato con ID Property11.</span><span class="sxs-lookup"><span data-stu-id="080f0-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="080f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="080f0-110">PARAMETERS</span></span>

### <span data-ttu-id="080f0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="080f0-111">-Context</span></span>
<span data-ttu-id="080f0-112">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="080f0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="080f0-113">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="080f0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="080f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080f0-114">-DefaultProfile</span></span>
<span data-ttu-id="080f0-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="080f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="080f0-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="080f0-116">-NamedValueId</span></span>
<span data-ttu-id="080f0-117">Identificatore del valore denominato esistente.</span><span class="sxs-lookup"><span data-stu-id="080f0-117">Identifier of existing named value.</span></span>
<span data-ttu-id="080f0-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="080f0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="080f0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="080f0-119">-PassThru</span></span>
<span data-ttu-id="080f0-120">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="080f0-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="080f0-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="080f0-121">This parameter is optional.</span></span>
<span data-ttu-id="080f0-122">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="080f0-122">Default value is false.</span></span>

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

### <span data-ttu-id="080f0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="080f0-123">-Confirm</span></span>
<span data-ttu-id="080f0-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="080f0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="080f0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="080f0-125">-WhatIf</span></span>
<span data-ttu-id="080f0-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="080f0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="080f0-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="080f0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="080f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080f0-128">CommonParameters</span></span>
<span data-ttu-id="080f0-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="080f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080f0-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="080f0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080f0-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="080f0-131">INPUTS</span></span>

### <span data-ttu-id="080f0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="080f0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="080f0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="080f0-133">System.String</span></span>

### <span data-ttu-id="080f0-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="080f0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="080f0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="080f0-135">OUTPUTS</span></span>

### <span data-ttu-id="080f0-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="080f0-136">System.Boolean</span></span>

## <span data-ttu-id="080f0-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="080f0-137">NOTES</span></span>

## <span data-ttu-id="080f0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="080f0-138">RELATED LINKS</span></span>
