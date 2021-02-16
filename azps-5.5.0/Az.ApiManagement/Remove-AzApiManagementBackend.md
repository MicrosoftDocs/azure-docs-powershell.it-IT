---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199742"
---
# <span data-ttu-id="fa108-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa108-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="fa108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa108-102">SYNOPSIS</span></span>
<span data-ttu-id="fa108-103">Rimuove un back-end.</span><span class="sxs-lookup"><span data-stu-id="fa108-103">Removes a Backend.</span></span>

## <span data-ttu-id="fa108-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa108-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa108-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa108-105">DESCRIPTION</span></span>
<span data-ttu-id="fa108-106">Rimuove un back-end specificato dall'identificatore dalla gestione delle api.</span><span class="sxs-lookup"><span data-stu-id="fa108-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="fa108-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa108-107">EXAMPLES</span></span>

### <span data-ttu-id="fa108-108">Esempio 1: Rimuovere il back-end 123</span><span class="sxs-lookup"><span data-stu-id="fa108-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="fa108-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa108-109">PARAMETERS</span></span>

### <span data-ttu-id="fa108-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="fa108-110">-BackendId</span></span>
<span data-ttu-id="fa108-111">Identificatore del back-end esistente.</span><span class="sxs-lookup"><span data-stu-id="fa108-111">Identifier of existing backend.</span></span>
<span data-ttu-id="fa108-112">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fa108-112">This parameter is required.</span></span>

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

### <span data-ttu-id="fa108-113">-Context</span><span class="sxs-lookup"><span data-stu-id="fa108-113">-Context</span></span>
<span data-ttu-id="fa108-114">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fa108-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fa108-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fa108-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fa108-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa108-116">-DefaultProfile</span></span>
<span data-ttu-id="fa108-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa108-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa108-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa108-118">-PassThru</span></span>
<span data-ttu-id="fa108-119">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="fa108-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fa108-120">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fa108-120">This parameter is optional.</span></span>
<span data-ttu-id="fa108-121">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="fa108-121">Default value is false.</span></span>

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

### <span data-ttu-id="fa108-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa108-122">-Confirm</span></span>
<span data-ttu-id="fa108-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa108-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa108-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa108-124">-WhatIf</span></span>
<span data-ttu-id="fa108-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa108-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa108-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa108-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa108-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa108-127">CommonParameters</span></span>
<span data-ttu-id="fa108-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa108-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa108-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa108-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa108-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa108-130">INPUTS</span></span>

### <span data-ttu-id="fa108-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fa108-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fa108-132">System.String</span><span class="sxs-lookup"><span data-stu-id="fa108-132">System.String</span></span>

### <span data-ttu-id="fa108-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa108-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa108-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa108-134">OUTPUTS</span></span>

### <span data-ttu-id="fa108-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa108-135">System.Boolean</span></span>

## <span data-ttu-id="fa108-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa108-136">NOTES</span></span>

## <span data-ttu-id="fa108-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa108-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa108-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa108-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="fa108-139">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa108-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="fa108-140">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="fa108-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="fa108-141">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="fa108-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="fa108-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="fa108-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
