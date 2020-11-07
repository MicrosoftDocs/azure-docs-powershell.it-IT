---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517632"
---
# <span data-ttu-id="b1f52-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f52-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="b1f52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1f52-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f52-103">Rimuove un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="b1f52-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1f52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1f52-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1f52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1f52-105">DESCRIPTION</span></span>
<span data-ttu-id="b1f52-106">Il cmdlet **Remove-AzureRmAutomationCertificate** rimuove un certificato da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b1f52-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="b1f52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1f52-107">EXAMPLES</span></span>

### <span data-ttu-id="b1f52-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="b1f52-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b1f52-109">Questo comando rimuove un certificato denominato Cert01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b1f52-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b1f52-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1f52-110">PARAMETERS</span></span>

### <span data-ttu-id="b1f52-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1f52-111">-AutomationAccountName</span></span>
<span data-ttu-id="b1f52-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="b1f52-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="b1f52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f52-113">-DefaultProfile</span></span>
<span data-ttu-id="b1f52-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b1f52-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1f52-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1f52-115">-Name</span></span>
<span data-ttu-id="b1f52-116">Specifica il nome del certificato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f52-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1f52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f52-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1f52-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="b1f52-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="b1f52-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1f52-119">-Confirm</span></span>
<span data-ttu-id="b1f52-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1f52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1f52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1f52-121">-WhatIf</span></span>
<span data-ttu-id="b1f52-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f52-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1f52-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1f52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1f52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f52-124">CommonParameters</span></span>
<span data-ttu-id="b1f52-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f52-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1f52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f52-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1f52-127">INPUTS</span></span>

### <span data-ttu-id="b1f52-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b1f52-128">System.String</span></span>

## <span data-ttu-id="b1f52-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1f52-129">OUTPUTS</span></span>

### <span data-ttu-id="b1f52-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b1f52-130">System.Void</span></span>

## <span data-ttu-id="b1f52-131">Note</span><span class="sxs-lookup"><span data-stu-id="b1f52-131">NOTES</span></span>

## <span data-ttu-id="b1f52-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1f52-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1f52-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f52-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="b1f52-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f52-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="b1f52-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1f52-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)

