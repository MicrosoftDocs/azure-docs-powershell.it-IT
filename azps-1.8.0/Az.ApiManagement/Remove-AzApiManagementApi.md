---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: df342b3ec96f8bfa8ba882bac2ae620456286012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852498"
---
# <span data-ttu-id="8d311-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="8d311-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d311-102">SYNOPSIS</span></span>
<span data-ttu-id="8d311-103">Rimuove un'API.</span><span class="sxs-lookup"><span data-stu-id="8d311-103">Removes an API.</span></span>

## <span data-ttu-id="8d311-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d311-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d311-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d311-105">DESCRIPTION</span></span>
<span data-ttu-id="8d311-106">Il cmdlet **Remove-AzApiManagementApi** rimuove un'API esistente.</span><span class="sxs-lookup"><span data-stu-id="8d311-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="8d311-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d311-107">EXAMPLES</span></span>

### <span data-ttu-id="8d311-108">Esempio 1: rimuovere un'API</span><span class="sxs-lookup"><span data-stu-id="8d311-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="8d311-109">Questo comando rimuove l'API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="8d311-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="8d311-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d311-110">PARAMETERS</span></span>

### <span data-ttu-id="8d311-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8d311-111">-ApiId</span></span>
<span data-ttu-id="8d311-112">Specifica l'ID dell'API Remove.</span><span class="sxs-lookup"><span data-stu-id="8d311-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="8d311-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8d311-113">-Context</span></span>
<span data-ttu-id="8d311-114">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8d311-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8d311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d311-115">-DefaultProfile</span></span>
<span data-ttu-id="8d311-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d311-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d311-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d311-117">-PassThru</span></span>
<span data-ttu-id="8d311-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="8d311-118">passthru</span></span>

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

### <span data-ttu-id="8d311-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8d311-119">-Confirm</span></span>
<span data-ttu-id="8d311-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d311-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d311-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d311-121">-WhatIf</span></span>
<span data-ttu-id="8d311-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d311-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d311-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d311-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d311-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d311-124">CommonParameters</span></span>
<span data-ttu-id="8d311-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d311-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d311-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d311-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d311-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d311-127">INPUTS</span></span>

### <span data-ttu-id="8d311-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d311-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d311-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8d311-129">System.String</span></span>

### <span data-ttu-id="8d311-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d311-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d311-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d311-131">OUTPUTS</span></span>

### <span data-ttu-id="8d311-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d311-132">System.Boolean</span></span>

## <span data-ttu-id="8d311-133">Note</span><span class="sxs-lookup"><span data-stu-id="8d311-133">NOTES</span></span>

## <span data-ttu-id="8d311-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d311-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d311-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="8d311-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="8d311-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="8d311-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="8d311-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d311-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


