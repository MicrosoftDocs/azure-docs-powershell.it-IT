---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: f10bd8d57cd70004ed37f16234aa72dd3a1a8ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993060"
---
# <span data-ttu-id="6f576-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6f576-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="6f576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f576-102">SYNOPSIS</span></span>
<span data-ttu-id="6f576-103">Recupera le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="6f576-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="6f576-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f576-104">SYNTAX</span></span>

### <span data-ttu-id="6f576-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f576-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f576-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f576-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f576-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6f576-107">DESCRIPTION</span></span>
<span data-ttu-id="6f576-108">Il cmdlet **Get-AzAutomationCredential** ottiene una o più credenziali di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f576-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="6f576-109">Per impostazione predefinita, vengono restituite tutte le credenziali.</span><span class="sxs-lookup"><span data-stu-id="6f576-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="6f576-110">Specificare il nome di una credenziali per ottenere una specifica credenziali.</span><span class="sxs-lookup"><span data-stu-id="6f576-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="6f576-111">Ai fini della sicurezza, questo cmdlet non restituisce password per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="6f576-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="6f576-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f576-112">EXAMPLES</span></span>

### <span data-ttu-id="6f576-113">Esempio 1: Ottenere tutte le credenziali</span><span class="sxs-lookup"><span data-stu-id="6f576-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6f576-114">Questo comando recupera i metadati per tutte le credenziali dell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6f576-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6f576-115">Esempio 2: Ottenere le credenziali</span><span class="sxs-lookup"><span data-stu-id="6f576-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="6f576-116">Questo comando recupera i metadati per le credenziali contosoCredential nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6f576-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6f576-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f576-117">PARAMETERS</span></span>

### <span data-ttu-id="6f576-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f576-118">-AutomationAccountName</span></span>
<span data-ttu-id="6f576-119">Specifica il nome dell'account di automazione per cui il cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="6f576-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6f576-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f576-120">-DefaultProfile</span></span>
<span data-ttu-id="6f576-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6f576-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f576-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6f576-122">-Name</span></span>
<span data-ttu-id="6f576-123">Specifica il nome delle credenziali da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6f576-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f576-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f576-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f576-125">Specifica il gruppo di risorse per cui questo cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="6f576-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6f576-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f576-126">CommonParameters</span></span>
<span data-ttu-id="6f576-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f576-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f576-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f576-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f576-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="6f576-129">INPUTS</span></span>

### <span data-ttu-id="6f576-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6f576-130">System.String</span></span>

## <span data-ttu-id="6f576-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f576-131">OUTPUTS</span></span>

### <span data-ttu-id="6f576-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6f576-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6f576-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="6f576-133">NOTES</span></span>

## <span data-ttu-id="6f576-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f576-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f576-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6f576-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="6f576-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6f576-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="6f576-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6f576-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


