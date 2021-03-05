---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: c243cd47300d2b361e37766ab7e2e5bc906cb2ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965421"
---
# <span data-ttu-id="f8847-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8847-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="f8847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8847-102">SYNOPSIS</span></span>
<span data-ttu-id="f8847-103">Configura un gruppo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8847-103">Configures an API management group.</span></span>

## <span data-ttu-id="f8847-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8847-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8847-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8847-105">DESCRIPTION</span></span>
<span data-ttu-id="f8847-106">Il cmdlet **Set-AzApiManagementGroup** configura un gruppo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="f8847-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="f8847-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8847-107">EXAMPLES</span></span>

### <span data-ttu-id="f8847-108">Esempio 1: Configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="f8847-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="f8847-109">Questo comando configura un gruppo di gestione denominato Group0001.</span><span class="sxs-lookup"><span data-stu-id="f8847-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="f8847-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8847-110">PARAMETERS</span></span>

### <span data-ttu-id="f8847-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f8847-111">-Context</span></span>
<span data-ttu-id="f8847-112">Specifica un'istanza di un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f8847-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f8847-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8847-113">-DefaultProfile</span></span>
<span data-ttu-id="f8847-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8847-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8847-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8847-115">-Description</span></span>
<span data-ttu-id="f8847-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f8847-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8847-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f8847-117">-GroupId</span></span>
<span data-ttu-id="f8847-118">Specifica l'identificatore del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f8847-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="f8847-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f8847-119">-Name</span></span>
<span data-ttu-id="f8847-120">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="f8847-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8847-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8847-121">-PassThru</span></span>
<span data-ttu-id="f8847-122">passthru</span><span class="sxs-lookup"><span data-stu-id="f8847-122">passthru</span></span>

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

### <span data-ttu-id="f8847-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8847-123">-Confirm</span></span>
<span data-ttu-id="f8847-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8847-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8847-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8847-125">-WhatIf</span></span>
<span data-ttu-id="f8847-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8847-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8847-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8847-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8847-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8847-128">CommonParameters</span></span>
<span data-ttu-id="f8847-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8847-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8847-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8847-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8847-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8847-131">INPUTS</span></span>

### <span data-ttu-id="f8847-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f8847-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8847-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f8847-133">System.String</span></span>

### <span data-ttu-id="f8847-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8847-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8847-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8847-135">OUTPUTS</span></span>

### <span data-ttu-id="f8847-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8847-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="f8847-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8847-137">NOTES</span></span>

## <span data-ttu-id="f8847-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8847-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8847-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8847-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="f8847-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8847-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="f8847-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f8847-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


