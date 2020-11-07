---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: d79f46e645bb5889c58aaca4b3fbdd046be5c756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686871"
---
# <span data-ttu-id="c90e9-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c90e9-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="c90e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c90e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c90e9-103">Ottiene gli account di automazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c90e9-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c90e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c90e9-104">SYNTAX</span></span>

### <span data-ttu-id="c90e9-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c90e9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c90e9-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c90e9-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c90e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c90e9-107">DESCRIPTION</span></span>
<span data-ttu-id="c90e9-108">Il cmdlet **Get-AzureRmAutomationAccount** ottiene gli account di automazione Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c90e9-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="c90e9-109">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="c90e9-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="c90e9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c90e9-110">EXAMPLES</span></span>

### <span data-ttu-id="c90e9-111">Esempio 1: ottenere tutti gli account</span><span class="sxs-lookup"><span data-stu-id="c90e9-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="c90e9-112">Questo comando consente di ottenere tutti gli account di automazione nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="c90e9-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="c90e9-113">Esempio 2: ottenere un account</span><span class="sxs-lookup"><span data-stu-id="c90e9-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="c90e9-114">Questo comando ottiene l'account di automazione denominato ContosoAutomationAccount nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c90e9-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c90e9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c90e9-115">PARAMETERS</span></span>

### <span data-ttu-id="c90e9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c90e9-116">-Name</span></span>
<span data-ttu-id="c90e9-117">Specifica il nome dell'account di automazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c90e9-117">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c90e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c90e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="c90e9-119">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene gli account di automazione.</span><span class="sxs-lookup"><span data-stu-id="c90e9-119">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="c90e9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90e9-120">-DefaultProfile</span></span>
<span data-ttu-id="c90e9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c90e9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c90e9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90e9-122">CommonParameters</span></span>
<span data-ttu-id="c90e9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90e9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90e9-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c90e9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90e9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c90e9-125">INPUTS</span></span>

## <span data-ttu-id="c90e9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c90e9-126">OUTPUTS</span></span>

### <span data-ttu-id="c90e9-127">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c90e9-127">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="c90e9-128">Note</span><span class="sxs-lookup"><span data-stu-id="c90e9-128">NOTES</span></span>

## <span data-ttu-id="c90e9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c90e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="c90e9-130">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c90e9-130">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="c90e9-131">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c90e9-131">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="c90e9-132">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="c90e9-132">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


