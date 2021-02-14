---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197182"
---
# <span data-ttu-id="c71cc-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c71cc-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="c71cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c71cc-102">SYNOPSIS</span></span>
<span data-ttu-id="c71cc-103">Rimuove un gruppo di gestione delle API esistente.</span><span class="sxs-lookup"><span data-stu-id="c71cc-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="c71cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c71cc-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c71cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c71cc-105">DESCRIPTION</span></span>
<span data-ttu-id="c71cc-106">Il cmdlet **Remove-AzApiManagementGroup** rimuove un gruppo di gestione delle API esistente.</span><span class="sxs-lookup"><span data-stu-id="c71cc-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="c71cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c71cc-107">EXAMPLES</span></span>

### <span data-ttu-id="c71cc-108">Esempio 1: Rimuovere un gruppo di gestione esistente</span><span class="sxs-lookup"><span data-stu-id="c71cc-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="c71cc-109">Questo comando rimuove un gruppo di gestione esistente denominato Group0001 e non richiede conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="c71cc-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="c71cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c71cc-110">PARAMETERS</span></span>

### <span data-ttu-id="c71cc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c71cc-111">-Context</span></span>
<span data-ttu-id="c71cc-112">Specifica l'istanza di un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c71cc-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c71cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71cc-113">-DefaultProfile</span></span>
<span data-ttu-id="c71cc-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c71cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c71cc-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c71cc-115">-GroupId</span></span>
<span data-ttu-id="c71cc-116">Specifica l'identificatore di un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c71cc-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="c71cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c71cc-117">-PassThru</span></span>
<span data-ttu-id="c71cc-118">Indica che questo cmdlet restituisce il valore $True se ha esito positivo oppure un valore di $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c71cc-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="c71cc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c71cc-119">-Confirm</span></span>
<span data-ttu-id="c71cc-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71cc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71cc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71cc-121">-WhatIf</span></span>
<span data-ttu-id="c71cc-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71cc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c71cc-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71cc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71cc-124">CommonParameters</span></span>
<span data-ttu-id="c71cc-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71cc-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c71cc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71cc-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="c71cc-127">INPUTS</span></span>

### <span data-ttu-id="c71cc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c71cc-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c71cc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c71cc-129">System.String</span></span>

### <span data-ttu-id="c71cc-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c71cc-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c71cc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c71cc-131">OUTPUTS</span></span>

### <span data-ttu-id="c71cc-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c71cc-132">System.Boolean</span></span>

## <span data-ttu-id="c71cc-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c71cc-133">NOTES</span></span>

## <span data-ttu-id="c71cc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c71cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="c71cc-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c71cc-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="c71cc-136">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c71cc-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="c71cc-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c71cc-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


