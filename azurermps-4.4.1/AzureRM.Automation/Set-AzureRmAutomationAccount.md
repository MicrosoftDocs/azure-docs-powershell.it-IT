---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511355"
---
# <span data-ttu-id="df7af-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="df7af-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="df7af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df7af-102">SYNOPSIS</span></span>
<span data-ttu-id="df7af-103">Modifica un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="df7af-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df7af-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df7af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df7af-105">DESCRIPTION</span></span>
<span data-ttu-id="df7af-106">Il cmdlet **set-AzureRmAutomationAccount** modifica un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="df7af-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="df7af-107">Per altre informazioni sugli account di automazione, vedere il cmdlet New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="df7af-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="df7af-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df7af-108">EXAMPLES</span></span>

### <span data-ttu-id="df7af-109">Esempio 1: impostare i tag per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="df7af-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="df7af-110">Il primo comando assegna due coppie chiave/valore alla variabile $Tags.</span><span class="sxs-lookup"><span data-stu-id="df7af-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="df7af-111">Il secondo comando imposta i tag in $Tags per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="df7af-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="df7af-112">Esempio 2: cambiare il piano per un account di automazione</span><span class="sxs-lookup"><span data-stu-id="df7af-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="df7af-113">Questo comando imposta il piano su Basic per l'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="df7af-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="df7af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df7af-114">PARAMETERS</span></span>

### <span data-ttu-id="df7af-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="df7af-115">-Name</span></span>
<span data-ttu-id="df7af-116">Specifica il nome dell'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7af-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7af-117">-Piano</span><span class="sxs-lookup"><span data-stu-id="df7af-117">-Plan</span></span>
<span data-ttu-id="df7af-118">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="df7af-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="df7af-119">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="df7af-119">Valid values are:</span></span>

- <span data-ttu-id="df7af-120">Base</span><span class="sxs-lookup"><span data-stu-id="df7af-120">Basic</span></span>
- <span data-ttu-id="df7af-121">Gratuito</span><span class="sxs-lookup"><span data-stu-id="df7af-121">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7af-122">-ResourceGroupName</span></span>
<span data-ttu-id="df7af-123">Specifica il nome di un gruppo di risorse che contiene l'account di automazione modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df7af-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="df7af-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="df7af-124">-Tags</span></span>
<span data-ttu-id="df7af-125">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="df7af-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="df7af-126">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="df7af-126">For example:</span></span>

<span data-ttu-id="df7af-127">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="df7af-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7af-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df7af-128">-DefaultProfile</span></span>
<span data-ttu-id="df7af-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df7af-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df7af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7af-130">CommonParameters</span></span>
<span data-ttu-id="df7af-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7af-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7af-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7af-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df7af-133">INPUTS</span></span>

## <span data-ttu-id="df7af-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df7af-134">OUTPUTS</span></span>

### <span data-ttu-id="df7af-135">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="df7af-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="df7af-136">Note</span><span class="sxs-lookup"><span data-stu-id="df7af-136">NOTES</span></span>

## <span data-ttu-id="df7af-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df7af-137">RELATED LINKS</span></span>

[<span data-ttu-id="df7af-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="df7af-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="df7af-139">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="df7af-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="df7af-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="df7af-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
