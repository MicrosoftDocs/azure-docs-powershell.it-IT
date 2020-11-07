---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: ff8a4427a909af35d8e8a910210e559212a6b7c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675940"
---
# <span data-ttu-id="e4e17-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4e17-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="e4e17-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4e17-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e17-103">Rimuove un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="e4e17-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="e4e17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4e17-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4e17-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4e17-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e17-106">Il cmdlet **Remove-AzApiManagementLogger** rimuove un **logger** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e17-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="e4e17-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4e17-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e17-108">Esempio 1: rimuovere un logger</span><span class="sxs-lookup"><span data-stu-id="e4e17-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="e4e17-109">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="e4e17-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="e4e17-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4e17-110">PARAMETERS</span></span>

### <span data-ttu-id="e4e17-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e4e17-111">-Context</span></span>
<span data-ttu-id="e4e17-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e4e17-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e4e17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e17-113">-DefaultProfile</span></span>
<span data-ttu-id="e4e17-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4e17-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e17-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e4e17-115">-LoggerId</span></span>
<span data-ttu-id="e4e17-116">Specifica l'ID del logger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e4e17-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="e4e17-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4e17-117">-PassThru</span></span>
<span data-ttu-id="e4e17-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e4e17-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="e4e17-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4e17-119">-Confirm</span></span>
<span data-ttu-id="e4e17-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e17-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e17-121">-WhatIf</span></span>
<span data-ttu-id="e4e17-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4e17-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e17-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4e17-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e17-124">CommonParameters</span></span>
<span data-ttu-id="e4e17-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e17-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4e17-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e17-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4e17-127">INPUTS</span></span>

### <span data-ttu-id="e4e17-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e4e17-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4e17-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e4e17-129">System.String</span></span>

### <span data-ttu-id="e4e17-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e4e17-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e4e17-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4e17-131">OUTPUTS</span></span>

### <span data-ttu-id="e4e17-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4e17-132">System.Boolean</span></span>

## <span data-ttu-id="e4e17-133">Note</span><span class="sxs-lookup"><span data-stu-id="e4e17-133">NOTES</span></span>

## <span data-ttu-id="e4e17-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4e17-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4e17-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4e17-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="e4e17-136">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4e17-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="e4e17-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e4e17-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


