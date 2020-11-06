---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518396"
---
# <span data-ttu-id="6c644-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c644-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="6c644-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c644-102">SYNOPSIS</span></span>
<span data-ttu-id="6c644-103">Rimuove un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="6c644-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c644-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c644-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c644-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c644-105">DESCRIPTION</span></span>
<span data-ttu-id="6c644-106">Il cmdlet **Remove-AzureRmAutomationCertificate** rimuove un certificato da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6c644-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="6c644-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c644-107">EXAMPLES</span></span>

### <span data-ttu-id="6c644-108">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="6c644-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6c644-109">Questo comando rimuove un certificato denominato Cert01 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6c644-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6c644-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c644-110">PARAMETERS</span></span>

### <span data-ttu-id="6c644-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c644-111">-AutomationAccountName</span></span>
<span data-ttu-id="6c644-112">Specifica il nome dell'account di automazione per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="6c644-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="6c644-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c644-113">-Name</span></span>
<span data-ttu-id="6c644-114">Specifica il nome del certificato rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c644-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c644-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c644-115">-ResourceGroupName</span></span>
<span data-ttu-id="6c644-116">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="6c644-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="6c644-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c644-117">-Confirm</span></span>
<span data-ttu-id="6c644-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c644-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c644-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c644-119">-WhatIf</span></span>
<span data-ttu-id="6c644-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c644-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c644-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c644-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c644-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c644-122">-DefaultProfile</span></span>
<span data-ttu-id="6c644-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c644-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c644-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c644-124">CommonParameters</span></span>
<span data-ttu-id="6c644-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c644-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c644-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c644-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c644-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c644-127">INPUTS</span></span>

## <span data-ttu-id="6c644-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c644-128">OUTPUTS</span></span>

## <span data-ttu-id="6c644-129">Note</span><span class="sxs-lookup"><span data-stu-id="6c644-129">NOTES</span></span>

## <span data-ttu-id="6c644-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c644-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c644-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c644-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6c644-132">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c644-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="6c644-133">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c644-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


