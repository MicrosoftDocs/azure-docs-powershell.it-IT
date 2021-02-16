---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199710"
---
# <span data-ttu-id="0b645-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b645-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="0b645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b645-102">SYNOPSIS</span></span>
<span data-ttu-id="0b645-103">Configura un gruppo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="0b645-103">Configures an API management group.</span></span>

## <span data-ttu-id="0b645-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b645-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b645-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b645-105">DESCRIPTION</span></span>
<span data-ttu-id="0b645-106">Il **cmdlet Set-AzApiManagementGroup** configura un gruppo di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="0b645-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="0b645-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b645-107">EXAMPLES</span></span>

### <span data-ttu-id="0b645-108">Esempio 1: Configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="0b645-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="0b645-109">Questo comando configura un gruppo di gestione denominato Group0001.</span><span class="sxs-lookup"><span data-stu-id="0b645-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="0b645-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b645-110">PARAMETERS</span></span>

### <span data-ttu-id="0b645-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0b645-111">-Context</span></span>
<span data-ttu-id="0b645-112">Specifica un'istanza di un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="0b645-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0b645-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b645-113">-DefaultProfile</span></span>
<span data-ttu-id="0b645-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b645-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b645-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b645-115">-Description</span></span>
<span data-ttu-id="0b645-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0b645-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="0b645-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0b645-117">-GroupId</span></span>
<span data-ttu-id="0b645-118">Specifica l'identificatore del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0b645-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="0b645-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0b645-119">-Name</span></span>
<span data-ttu-id="0b645-120">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="0b645-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="0b645-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b645-121">-PassThru</span></span>
<span data-ttu-id="0b645-122">passthru</span><span class="sxs-lookup"><span data-stu-id="0b645-122">passthru</span></span>

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

### <span data-ttu-id="0b645-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b645-123">-Confirm</span></span>
<span data-ttu-id="0b645-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b645-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b645-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b645-125">-WhatIf</span></span>
<span data-ttu-id="0b645-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b645-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b645-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b645-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b645-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b645-128">CommonParameters</span></span>
<span data-ttu-id="0b645-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b645-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b645-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b645-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b645-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b645-131">INPUTS</span></span>

### <span data-ttu-id="0b645-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0b645-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b645-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0b645-133">System.String</span></span>

### <span data-ttu-id="0b645-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0b645-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b645-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b645-135">OUTPUTS</span></span>

### <span data-ttu-id="0b645-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b645-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="0b645-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b645-137">NOTES</span></span>

## <span data-ttu-id="0b645-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b645-138">RELATED LINKS</span></span>

[<span data-ttu-id="0b645-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b645-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="0b645-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b645-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="0b645-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0b645-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


