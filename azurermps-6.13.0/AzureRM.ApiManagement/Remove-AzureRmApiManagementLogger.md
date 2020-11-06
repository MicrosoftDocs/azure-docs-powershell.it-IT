---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementLogger.md
ms.openlocfilehash: 135dced6c66f1212f172a2c435a7468b16e71708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507727"
---
# <span data-ttu-id="ddf36-101">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ddf36-101">Remove-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="ddf36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddf36-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf36-103">Rimuove un logger di gestione API.</span><span class="sxs-lookup"><span data-stu-id="ddf36-103">Removes an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddf36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddf36-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddf36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddf36-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf36-106">Il cmdlet **Remove-AzureRmApiManagementLogger** rimuove un **logger** di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf36-106">The **Remove-AzureRmApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="ddf36-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddf36-107">EXAMPLES</span></span>

### <span data-ttu-id="ddf36-108">Esempio 1: rimuovere un logger</span><span class="sxs-lookup"><span data-stu-id="ddf36-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="ddf36-109">Questo comando rimuove un logger con ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="ddf36-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="ddf36-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddf36-110">PARAMETERS</span></span>

### <span data-ttu-id="ddf36-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ddf36-111">-Context</span></span>
<span data-ttu-id="ddf36-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ddf36-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ddf36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf36-113">-DefaultProfile</span></span>
<span data-ttu-id="ddf36-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddf36-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddf36-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="ddf36-115">-LoggerId</span></span>
<span data-ttu-id="ddf36-116">Specifica l'ID del logger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ddf36-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="ddf36-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ddf36-117">-PassThru</span></span>
<span data-ttu-id="ddf36-118">Indica che questo cmdlet restituisce un valore di $True se l'operazione viene eseguita correttamente o $False in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ddf36-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="ddf36-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ddf36-119">-Confirm</span></span>
<span data-ttu-id="ddf36-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddf36-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddf36-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddf36-121">-WhatIf</span></span>
<span data-ttu-id="ddf36-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddf36-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddf36-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ddf36-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddf36-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf36-124">CommonParameters</span></span>
<span data-ttu-id="ddf36-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf36-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf36-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf36-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf36-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddf36-127">INPUTS</span></span>

### <span data-ttu-id="ddf36-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ddf36-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ddf36-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ddf36-129">System.String</span></span>

### <span data-ttu-id="ddf36-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddf36-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ddf36-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddf36-131">OUTPUTS</span></span>

### <span data-ttu-id="ddf36-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ddf36-132">System.Boolean</span></span>

## <span data-ttu-id="ddf36-133">Note</span><span class="sxs-lookup"><span data-stu-id="ddf36-133">NOTES</span></span>

## <span data-ttu-id="ddf36-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddf36-134">RELATED LINKS</span></span>

[<span data-ttu-id="ddf36-135">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ddf36-135">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="ddf36-136">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ddf36-136">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="ddf36-137">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="ddf36-137">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


