---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: 7bdf37996fb5d407d3961ddacee4701acce2baaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952941"
---
# <span data-ttu-id="770cd-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="770cd-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="770cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770cd-102">SYNOPSIS</span></span>
<span data-ttu-id="770cd-103">Rimuove un registro gestione API.</span><span class="sxs-lookup"><span data-stu-id="770cd-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="770cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="770cd-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770cd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="770cd-105">DESCRIPTION</span></span>
<span data-ttu-id="770cd-106">Il cmdlet **Remove-AzApiManagementLogger rimuove** un cmdlet Azure API Management **Logger.**</span><span class="sxs-lookup"><span data-stu-id="770cd-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="770cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="770cd-107">EXAMPLES</span></span>

### <span data-ttu-id="770cd-108">Esempio 1: Rimuovere un logger</span><span class="sxs-lookup"><span data-stu-id="770cd-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="770cd-109">Questo comando rimuove un dispositivo che ha l'ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="770cd-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="770cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770cd-110">PARAMETERS</span></span>

### <span data-ttu-id="770cd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="770cd-111">-Context</span></span>
<span data-ttu-id="770cd-112">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="770cd-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="770cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770cd-113">-DefaultProfile</span></span>
<span data-ttu-id="770cd-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="770cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="770cd-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="770cd-115">-LoggerId</span></span>
<span data-ttu-id="770cd-116">Specifica l'ID del dispositivo di registrazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="770cd-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="770cd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="770cd-117">-PassThru</span></span>
<span data-ttu-id="770cd-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione riesce o se $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="770cd-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="770cd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="770cd-119">-Confirm</span></span>
<span data-ttu-id="770cd-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="770cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770cd-121">-WhatIf</span></span>
<span data-ttu-id="770cd-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="770cd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770cd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="770cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770cd-124">CommonParameters</span></span>
<span data-ttu-id="770cd-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770cd-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="770cd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770cd-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="770cd-127">INPUTS</span></span>

### <span data-ttu-id="770cd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="770cd-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="770cd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="770cd-129">System.String</span></span>

### <span data-ttu-id="770cd-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="770cd-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="770cd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="770cd-131">OUTPUTS</span></span>

### <span data-ttu-id="770cd-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="770cd-132">System.Boolean</span></span>

## <span data-ttu-id="770cd-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="770cd-133">NOTES</span></span>

## <span data-ttu-id="770cd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="770cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="770cd-135">Get-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="770cd-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="770cd-136">New-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="770cd-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="770cd-137">Set-AzApiManagementManagement</span><span class="sxs-lookup"><span data-stu-id="770cd-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


