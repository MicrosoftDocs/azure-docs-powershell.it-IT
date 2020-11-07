---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 2508732b703edf8a4251d305f4bc721eeeed70c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675897"
---
# <span data-ttu-id="c8398-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c8398-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="c8398-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8398-102">SYNOPSIS</span></span>
<span data-ttu-id="c8398-103">Configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="c8398-103">Configures an API management group.</span></span>

## <span data-ttu-id="c8398-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8398-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8398-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8398-105">DESCRIPTION</span></span>
<span data-ttu-id="c8398-106">Il cmdlet **set-AzApiManagementGroup** configura un gruppo di gestione API.</span><span class="sxs-lookup"><span data-stu-id="c8398-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="c8398-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8398-107">EXAMPLES</span></span>

### <span data-ttu-id="c8398-108">Esempio 1: configurare un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c8398-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="c8398-109">Questo comando configura un gruppo di gestione denominato Group0001.</span><span class="sxs-lookup"><span data-stu-id="c8398-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="c8398-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8398-110">PARAMETERS</span></span>

### <span data-ttu-id="c8398-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c8398-111">-Context</span></span>
<span data-ttu-id="c8398-112">Specifica un'istanza di un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c8398-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c8398-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8398-113">-DefaultProfile</span></span>
<span data-ttu-id="c8398-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8398-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8398-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8398-115">-Description</span></span>
<span data-ttu-id="c8398-116">Specifica la descrizione del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c8398-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="c8398-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c8398-117">-GroupId</span></span>
<span data-ttu-id="c8398-118">Specifica l'identificatore del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c8398-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="c8398-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8398-119">-Name</span></span>
<span data-ttu-id="c8398-120">Specifica il nome del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="c8398-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="c8398-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8398-121">-PassThru</span></span>
<span data-ttu-id="c8398-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="c8398-122">passthru</span></span>

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

### <span data-ttu-id="c8398-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8398-123">-Confirm</span></span>
<span data-ttu-id="c8398-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8398-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8398-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8398-125">-WhatIf</span></span>
<span data-ttu-id="c8398-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8398-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8398-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8398-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8398-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8398-128">CommonParameters</span></span>
<span data-ttu-id="c8398-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8398-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8398-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8398-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8398-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8398-131">INPUTS</span></span>

### <span data-ttu-id="c8398-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c8398-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c8398-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c8398-133">System.String</span></span>

### <span data-ttu-id="c8398-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c8398-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8398-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8398-135">OUTPUTS</span></span>

### <span data-ttu-id="c8398-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c8398-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c8398-137">Note</span><span class="sxs-lookup"><span data-stu-id="c8398-137">NOTES</span></span>

## <span data-ttu-id="c8398-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8398-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8398-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c8398-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="c8398-140">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c8398-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="c8398-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c8398-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


