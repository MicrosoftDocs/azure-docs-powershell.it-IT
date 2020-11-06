---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCredential.md
ms.openlocfilehash: 2c98cde73610a7a72b237bbe268f527fefaf71a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518391"
---
# <span data-ttu-id="da081-101">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da081-101">Remove-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="da081-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da081-102">SYNOPSIS</span></span>
<span data-ttu-id="da081-103">Rimuove una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="da081-103">Removes an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da081-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da081-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da081-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da081-105">DESCRIPTION</span></span>
<span data-ttu-id="da081-106">Il cmdlet **Remove-AzureRmAutomationCredential** consente di rimuovere una credenziale da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="da081-106">The **Remove-AzureRmAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="da081-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da081-107">EXAMPLES</span></span>

### <span data-ttu-id="da081-108">Esempio 1: rimuovere una credenziale</span><span class="sxs-lookup"><span data-stu-id="da081-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da081-109">Questo comando rimuove una credenziale denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="da081-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="da081-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da081-110">PARAMETERS</span></span>

### <span data-ttu-id="da081-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da081-111">-AutomationAccountName</span></span>
<span data-ttu-id="da081-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="da081-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da081-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="da081-113">-Name</span></span>
<span data-ttu-id="da081-114">Specifica il nome delle credenziali rimosse da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da081-114">Specifies the name of the credential that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da081-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da081-115">-ResourceGroupName</span></span>
<span data-ttu-id="da081-116">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove una credenziale.</span><span class="sxs-lookup"><span data-stu-id="da081-116">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da081-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da081-117">-Confirm</span></span>
<span data-ttu-id="da081-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da081-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da081-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da081-119">-WhatIf</span></span>
<span data-ttu-id="da081-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da081-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da081-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da081-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da081-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da081-122">-DefaultProfile</span></span>
<span data-ttu-id="da081-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da081-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da081-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da081-124">CommonParameters</span></span>
<span data-ttu-id="da081-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da081-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da081-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da081-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da081-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da081-127">INPUTS</span></span>

## <span data-ttu-id="da081-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da081-128">OUTPUTS</span></span>

## <span data-ttu-id="da081-129">Note</span><span class="sxs-lookup"><span data-stu-id="da081-129">NOTES</span></span>

## <span data-ttu-id="da081-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da081-130">RELATED LINKS</span></span>

[<span data-ttu-id="da081-131">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da081-131">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="da081-132">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da081-132">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="da081-133">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da081-133">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


