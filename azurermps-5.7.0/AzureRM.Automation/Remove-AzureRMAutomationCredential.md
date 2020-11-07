---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 11b6772325c3e5170c697b21d25092fd96f3e2e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688187"
---
# <span data-ttu-id="5bf06-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5bf06-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="5bf06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5bf06-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf06-103">Rimuove una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="5bf06-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bf06-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bf06-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf06-106">Il cmdlet **Remove-AzureRmAutomationCredential** consente di rimuovere una credenziale da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5bf06-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="5bf06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bf06-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf06-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="5bf06-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5bf06-109">Questo comando rimuove una credenziale denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5bf06-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5bf06-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5bf06-110">PARAMETERS</span></span>

### <span data-ttu-id="5bf06-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bf06-111">-AutomationAccountName</span></span>
<span data-ttu-id="5bf06-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="5bf06-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf06-113">-DefaultProfile</span></span>
<span data-ttu-id="5bf06-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5bf06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bf06-115">-Name</span></span>
<span data-ttu-id="5bf06-116">Specifica il nome delle credenziali rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf06-116">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf06-117">-ResourceGroupName</span></span>
<span data-ttu-id="5bf06-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="5bf06-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5bf06-119">-Confirm</span></span>
<span data-ttu-id="5bf06-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf06-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf06-121">-WhatIf</span></span>
<span data-ttu-id="5bf06-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bf06-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf06-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bf06-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf06-124">CommonParameters</span></span>
<span data-ttu-id="5bf06-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf06-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf06-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5bf06-127">INPUTS</span></span>

### <span data-ttu-id="5bf06-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5bf06-128">None</span></span>
<span data-ttu-id="5bf06-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5bf06-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bf06-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bf06-130">OUTPUTS</span></span>

## <span data-ttu-id="5bf06-131">Note</span><span class="sxs-lookup"><span data-stu-id="5bf06-131">NOTES</span></span>

## <span data-ttu-id="5bf06-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bf06-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bf06-133">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5bf06-133">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="5bf06-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5bf06-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="5bf06-135">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5bf06-135">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


