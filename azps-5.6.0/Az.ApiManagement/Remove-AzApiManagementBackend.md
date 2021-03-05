---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 9a5c4d553f425d7922fa927451ca9f3029a9f4b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972989"
---
# <span data-ttu-id="2354f-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2354f-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="2354f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2354f-102">SYNOPSIS</span></span>
<span data-ttu-id="2354f-103">Rimuove un back-end.</span><span class="sxs-lookup"><span data-stu-id="2354f-103">Removes a Backend.</span></span>

## <span data-ttu-id="2354f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2354f-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2354f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2354f-105">DESCRIPTION</span></span>
<span data-ttu-id="2354f-106">Rimuove un back-end specificato dall'identificatore da Gestione api.</span><span class="sxs-lookup"><span data-stu-id="2354f-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="2354f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2354f-107">EXAMPLES</span></span>

### <span data-ttu-id="2354f-108">Esempio 1: Rimuovere il back-end 123</span><span class="sxs-lookup"><span data-stu-id="2354f-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="2354f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2354f-109">PARAMETERS</span></span>

### <span data-ttu-id="2354f-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2354f-110">-BackendId</span></span>
<span data-ttu-id="2354f-111">Identificatore del back-end esistente.</span><span class="sxs-lookup"><span data-stu-id="2354f-111">Identifier of existing backend.</span></span>
<span data-ttu-id="2354f-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2354f-112">This parameter is required.</span></span>

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

### <span data-ttu-id="2354f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2354f-113">-Context</span></span>
<span data-ttu-id="2354f-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2354f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2354f-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2354f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2354f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2354f-116">-DefaultProfile</span></span>
<span data-ttu-id="2354f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2354f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2354f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2354f-118">-PassThru</span></span>
<span data-ttu-id="2354f-119">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="2354f-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2354f-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2354f-120">This parameter is optional.</span></span>
<span data-ttu-id="2354f-121">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2354f-121">Default value is false.</span></span>

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

### <span data-ttu-id="2354f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2354f-122">-Confirm</span></span>
<span data-ttu-id="2354f-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2354f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2354f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2354f-124">-WhatIf</span></span>
<span data-ttu-id="2354f-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2354f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2354f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2354f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2354f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2354f-127">CommonParameters</span></span>
<span data-ttu-id="2354f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2354f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2354f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2354f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2354f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="2354f-130">INPUTS</span></span>

### <span data-ttu-id="2354f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2354f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2354f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2354f-132">System.String</span></span>

### <span data-ttu-id="2354f-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2354f-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2354f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2354f-134">OUTPUTS</span></span>

### <span data-ttu-id="2354f-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2354f-135">System.Boolean</span></span>

## <span data-ttu-id="2354f-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2354f-136">NOTES</span></span>

## <span data-ttu-id="2354f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2354f-137">RELATED LINKS</span></span>

[<span data-ttu-id="2354f-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2354f-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="2354f-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2354f-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="2354f-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2354f-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="2354f-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2354f-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="2354f-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2354f-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
