---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675763"
---
# <span data-ttu-id="9e778-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e778-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="9e778-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e778-102">SYNOPSIS</span></span>
<span data-ttu-id="9e778-103">Crea un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-103">Creates an Automation account.</span></span>

## <span data-ttu-id="9e778-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e778-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e778-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e778-105">DESCRIPTION</span></span>
<span data-ttu-id="9e778-106">Il cmdlet **New-AzAutomationAccount** crea un account di automazione di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e778-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="9e778-107">Un account di automazione è un contenitore per le risorse di automazione che viene isolato dalle risorse di altri account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="9e778-108">Le risorse di automazione includono manuali operativi, configurazioni di configurazione dello stato (DSC) desiderate, processi e asset.</span><span class="sxs-lookup"><span data-stu-id="9e778-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="9e778-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e778-109">EXAMPLES</span></span>

### <span data-ttu-id="9e778-110">Esempio 1: creare un account di automazione</span><span class="sxs-lookup"><span data-stu-id="9e778-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e778-111">Questo comando crea un nuovo account di automazione denominato ContosoAutomationAccount nell'area est degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="9e778-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="9e778-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e778-112">PARAMETERS</span></span>

### <span data-ttu-id="9e778-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e778-113">-DefaultProfile</span></span>
<span data-ttu-id="9e778-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e778-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e778-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9e778-115">-Location</span></span>
<span data-ttu-id="9e778-116">Specifica la posizione in cui questo cmdlet crea l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="9e778-117">Per ottenere posizioni valide, usare il cmdlet Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="9e778-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="9e778-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e778-118">-Name</span></span>
<span data-ttu-id="9e778-119">Specifica un nome per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="9e778-120">-Piano</span><span class="sxs-lookup"><span data-stu-id="9e778-120">-Plan</span></span>
<span data-ttu-id="9e778-121">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="9e778-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="9e778-122">Valid values are:</span></span>
- <span data-ttu-id="9e778-123">Base</span><span class="sxs-lookup"><span data-stu-id="9e778-123">Basic</span></span>
- <span data-ttu-id="9e778-124">Gratuito</span><span class="sxs-lookup"><span data-stu-id="9e778-124">Free</span></span>

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

### <span data-ttu-id="9e778-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e778-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e778-126">Specifica il nome di un gruppo di risorse a cui questo cmdlet aggiunge un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="9e778-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="9e778-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e778-127">-Tags</span></span>
<span data-ttu-id="9e778-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9e778-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e778-129">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9e778-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e778-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e778-130">CommonParameters</span></span>
<span data-ttu-id="9e778-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e778-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e778-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e778-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e778-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e778-133">INPUTS</span></span>

### <span data-ttu-id="9e778-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e778-134">System.String</span></span>

### <span data-ttu-id="9e778-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9e778-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="9e778-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e778-136">OUTPUTS</span></span>

### <span data-ttu-id="9e778-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e778-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="9e778-138">Note</span><span class="sxs-lookup"><span data-stu-id="9e778-138">NOTES</span></span>

## <span data-ttu-id="9e778-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e778-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e778-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e778-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="9e778-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e778-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="9e778-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="9e778-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
