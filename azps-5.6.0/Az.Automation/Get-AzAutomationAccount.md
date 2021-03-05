---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: f88ff018f38040573783aff58287b4788017566a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996994"
---
# <span data-ttu-id="cb9ea-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb9ea-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="cb9ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cb9ea-103">Recupera gli account di automazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="cb9ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb9ea-104">SYNTAX</span></span>

### <span data-ttu-id="cb9ea-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb9ea-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb9ea-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cb9ea-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb9ea-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb9ea-107">DESCRIPTION</span></span>
<span data-ttu-id="cb9ea-108">Il cmdlet **Get-AzAutomationAccount** ottiene gli account di Automazione di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="cb9ea-109">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="cb9ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb9ea-110">EXAMPLES</span></span>

### <span data-ttu-id="cb9ea-111">Esempio 1: Ottenere tutti gli account</span><span class="sxs-lookup"><span data-stu-id="cb9ea-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="cb9ea-112">Questo comando recupera tutti gli account di automazione nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="cb9ea-113">Esempio 2: Ottenere un account</span><span class="sxs-lookup"><span data-stu-id="cb9ea-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="cb9ea-114">Questo comando recupera l'account di automazione denominato ContosoAutomationAccount nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="cb9ea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb9ea-115">PARAMETERS</span></span>

### <span data-ttu-id="cb9ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb9ea-116">-DefaultProfile</span></span>
<span data-ttu-id="cb9ea-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cb9ea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb9ea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cb9ea-118">-Name</span></span>
<span data-ttu-id="cb9ea-119">Specifica il nome dell'account di automazione che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb9ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb9ea-121">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene gli account di automazione.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb9ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb9ea-122">CommonParameters</span></span>
<span data-ttu-id="cb9ea-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb9ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb9ea-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb9ea-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb9ea-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb9ea-125">INPUTS</span></span>

### <span data-ttu-id="cb9ea-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cb9ea-126">System.String</span></span>

## <span data-ttu-id="cb9ea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb9ea-127">OUTPUTS</span></span>

### <span data-ttu-id="cb9ea-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb9ea-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="cb9ea-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb9ea-129">NOTES</span></span>

## <span data-ttu-id="cb9ea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb9ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb9ea-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb9ea-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="cb9ea-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb9ea-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="cb9ea-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb9ea-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


