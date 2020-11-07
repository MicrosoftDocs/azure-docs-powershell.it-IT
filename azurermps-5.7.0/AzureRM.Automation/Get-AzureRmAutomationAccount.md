---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688584"
---
# <span data-ttu-id="8fd52-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8fd52-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="8fd52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fd52-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd52-103">Ottiene gli account di automazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8fd52-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fd52-104">SYNTAX</span></span>

### <span data-ttu-id="8fd52-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8fd52-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fd52-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8fd52-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd52-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fd52-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd52-108">Il cmdlet **Get-AzureRmAutomationAccount** ottiene gli account di automazione Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8fd52-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="8fd52-109">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="8fd52-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8fd52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fd52-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd52-111">Esempio 1: ottenere tutti gli account</span><span class="sxs-lookup"><span data-stu-id="8fd52-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="8fd52-112">Questo comando consente di ottenere tutti gli account di automazione nel gruppo di risorse denominato ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="8fd52-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="8fd52-113">Esempio 2: ottenere un account</span><span class="sxs-lookup"><span data-stu-id="8fd52-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="8fd52-114">Questo comando ottiene l'account di automazione denominato ContosoAutomationAccount nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8fd52-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8fd52-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fd52-115">PARAMETERS</span></span>

### <span data-ttu-id="8fd52-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd52-116">-DefaultProfile</span></span>
<span data-ttu-id="8fd52-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8fd52-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fd52-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fd52-118">-Name</span></span>
<span data-ttu-id="8fd52-119">Specifica il nome dell'account di automazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd52-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd52-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd52-120">-ResourceGroupName</span></span>
<span data-ttu-id="8fd52-121">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene gli account di automazione.</span><span class="sxs-lookup"><span data-stu-id="8fd52-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd52-122">CommonParameters</span></span>
<span data-ttu-id="8fd52-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd52-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd52-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd52-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fd52-125">INPUTS</span></span>

### <span data-ttu-id="8fd52-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8fd52-126">None</span></span>
<span data-ttu-id="8fd52-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8fd52-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8fd52-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fd52-128">OUTPUTS</span></span>

### <span data-ttu-id="8fd52-129">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8fd52-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8fd52-130">Note</span><span class="sxs-lookup"><span data-stu-id="8fd52-130">NOTES</span></span>

## <span data-ttu-id="8fd52-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fd52-131">RELATED LINKS</span></span>

[<span data-ttu-id="8fd52-132">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8fd52-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="8fd52-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8fd52-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="8fd52-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8fd52-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


