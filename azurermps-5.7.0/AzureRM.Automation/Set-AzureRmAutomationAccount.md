---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: bbb90e728c9c43c011c4610ee47273af1fdae668
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518232"
---
# <span data-ttu-id="4af26-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4af26-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="4af26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4af26-102">SYNOPSIS</span></span>
<span data-ttu-id="4af26-103">Modifica un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="4af26-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4af26-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4af26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4af26-105">DESCRIPTION</span></span>
<span data-ttu-id="4af26-106">Il cmdlet **set-AzureRmAutomationAccount** modifica un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4af26-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="4af26-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="4af26-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="4af26-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4af26-108">EXAMPLES</span></span>

### <span data-ttu-id="4af26-109">Esempio 1: impostare i tag per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="4af26-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="4af26-110">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="4af26-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="4af26-111">Il secondo comando imposta i tag in $Tags per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4af26-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="4af26-112">Esempio 2: cambiare il piano per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="4af26-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="4af26-113">Questo comando imposta il piano su Basic per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4af26-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="4af26-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4af26-114">PARAMETERS</span></span>

### <span data-ttu-id="4af26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af26-115">-DefaultProfile</span></span>
<span data-ttu-id="4af26-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4af26-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4af26-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="4af26-117">-Name</span></span>
<span data-ttu-id="4af26-118">Specifica il nome dell'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af26-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af26-119">-Piano</span><span class="sxs-lookup"><span data-stu-id="4af26-119">-Plan</span></span>
<span data-ttu-id="4af26-120">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="4af26-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="4af26-121">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="4af26-121">Valid values are:</span></span>

- <span data-ttu-id="4af26-122">Base</span><span class="sxs-lookup"><span data-stu-id="4af26-122">Basic</span></span>
- <span data-ttu-id="4af26-123">Gratuito</span><span class="sxs-lookup"><span data-stu-id="4af26-123">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af26-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af26-124">-ResourceGroupName</span></span>
<span data-ttu-id="4af26-125">Specifica il nome di un gruppo di risorse che contiene l'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af26-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4af26-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4af26-126">-Tags</span></span>
<span data-ttu-id="4af26-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4af26-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4af26-128">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="4af26-128">For example:</span></span>

<span data-ttu-id="4af26-129">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4af26-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4af26-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af26-130">CommonParameters</span></span>
<span data-ttu-id="4af26-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af26-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af26-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af26-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af26-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4af26-133">INPUTS</span></span>

### <span data-ttu-id="4af26-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4af26-134">None</span></span>
<span data-ttu-id="4af26-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4af26-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4af26-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4af26-136">OUTPUTS</span></span>

### <span data-ttu-id="4af26-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4af26-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="4af26-138">Note</span><span class="sxs-lookup"><span data-stu-id="4af26-138">NOTES</span></span>

## <span data-ttu-id="4af26-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4af26-139">RELATED LINKS</span></span>

[<span data-ttu-id="4af26-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4af26-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="4af26-141">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4af26-141">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="4af26-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="4af26-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
