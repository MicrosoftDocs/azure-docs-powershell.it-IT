---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328420"
---
# <span data-ttu-id="a9a59-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a9a59-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="a9a59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9a59-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a59-103">Ottiene gli account di automazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9a59-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="a9a59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9a59-104">SYNTAX</span></span>

### <span data-ttu-id="a9a59-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9a59-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9a59-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9a59-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9a59-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9a59-107">DESCRIPTION</span></span>
<span data-ttu-id="a9a59-108">Il cmdlet **Get-AzAutomationAccount** ottiene gli account di automazione Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9a59-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="a9a59-109">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="a9a59-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="a9a59-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9a59-110">EXAMPLES</span></span>

### <span data-ttu-id="a9a59-111">Esempio 1: ottenere tutti gli account</span><span class="sxs-lookup"><span data-stu-id="a9a59-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="a9a59-112">Questo comando consente di ottenere tutti gli account di automazione nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="a9a59-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="a9a59-113">Esempio 2: ottenere un account</span><span class="sxs-lookup"><span data-stu-id="a9a59-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="a9a59-114">Questo comando ottiene l'account di automazione denominato ContosoAutomationAccount nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a9a59-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="a9a59-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9a59-115">PARAMETERS</span></span>

### <span data-ttu-id="a9a59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a59-116">-DefaultProfile</span></span>
<span data-ttu-id="a9a59-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a9a59-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9a59-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9a59-118">-Name</span></span>
<span data-ttu-id="a9a59-119">Specifica il nome dell'account di automazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9a59-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a9a59-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a59-120">-ResourceGroupName</span></span>
<span data-ttu-id="a9a59-121">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene gli account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a9a59-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="a9a59-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a59-122">CommonParameters</span></span>
<span data-ttu-id="a9a59-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a59-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a59-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a59-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a59-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9a59-125">INPUTS</span></span>

### <span data-ttu-id="a9a59-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a9a59-126">System.String</span></span>

## <span data-ttu-id="a9a59-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9a59-127">OUTPUTS</span></span>

### <span data-ttu-id="a9a59-128">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a9a59-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a9a59-129">Note</span><span class="sxs-lookup"><span data-stu-id="a9a59-129">NOTES</span></span>

## <span data-ttu-id="a9a59-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9a59-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9a59-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a9a59-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="a9a59-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a9a59-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="a9a59-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a9a59-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


