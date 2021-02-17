---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205530"
---
# <span data-ttu-id="5aaf4-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5aaf4-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="5aaf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aaf4-102">SYNOPSIS</span></span>
<span data-ttu-id="5aaf4-103">Rimuove un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="5aaf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5aaf4-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aaf4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5aaf4-105">DESCRIPTION</span></span>
<span data-ttu-id="5aaf4-106">Il cmdlet **Remove-AzAutomationCertificate** rimuove un certificato dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="5aaf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5aaf4-107">EXAMPLES</span></span>

### <span data-ttu-id="5aaf4-108">Esempio 1: Rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="5aaf4-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5aaf4-109">Questo comando rimuove un certificato denominato Cert01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5aaf4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aaf4-110">PARAMETERS</span></span>

### <span data-ttu-id="5aaf4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5aaf4-111">-AutomationAccountName</span></span>
<span data-ttu-id="5aaf4-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="5aaf4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aaf4-113">-DefaultProfile</span></span>
<span data-ttu-id="5aaf4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5aaf4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aaf4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5aaf4-115">-Name</span></span>
<span data-ttu-id="5aaf4-116">Specifica il nome del certificato rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5aaf4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aaf4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5aaf4-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="5aaf4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aaf4-119">-Confirm</span></span>
<span data-ttu-id="5aaf4-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aaf4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aaf4-121">-WhatIf</span></span>
<span data-ttu-id="5aaf4-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aaf4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aaf4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aaf4-124">CommonParameters</span></span>
<span data-ttu-id="5aaf4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aaf4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aaf4-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aaf4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aaf4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5aaf4-127">INPUTS</span></span>

### <span data-ttu-id="5aaf4-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5aaf4-128">System.String</span></span>

## <span data-ttu-id="5aaf4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5aaf4-129">OUTPUTS</span></span>

### <span data-ttu-id="5aaf4-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5aaf4-130">System.Void</span></span>

## <span data-ttu-id="5aaf4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5aaf4-131">NOTES</span></span>

## <span data-ttu-id="5aaf4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5aaf4-132">RELATED LINKS</span></span>

[<span data-ttu-id="5aaf4-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5aaf4-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="5aaf4-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5aaf4-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="5aaf4-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5aaf4-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


