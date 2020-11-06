---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510175"
---
# <span data-ttu-id="a3ccf-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a3ccf-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="a3ccf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ccf-103">Crea un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ccf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3ccf-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ccf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ccf-106">Il cmdlet **New-AzureRmAutomationAccount** crea un account di automazione di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="a3ccf-107">Un account di automazione è un contenitore per le risorse di automazione che viene isolato dalle risorse di altri account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="a3ccf-108">Le risorse di automazione includono manuali operativi, configurazioni di configurazione dello stato (DSC) desiderate, processi e asset.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="a3ccf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3ccf-109">EXAMPLES</span></span>

### <span data-ttu-id="a3ccf-110">Esempio 1: creare un account di automazione</span><span class="sxs-lookup"><span data-stu-id="a3ccf-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a3ccf-111">Questo comando crea un nuovo account di automazione denominato ContosoAutomationAccount nell'area est degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="a3ccf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3ccf-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ccf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ccf-113">-DefaultProfile</span></span>
<span data-ttu-id="a3ccf-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a3ccf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3ccf-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a3ccf-115">-Location</span></span>
<span data-ttu-id="a3ccf-116">Specifica la posizione in cui questo cmdlet crea l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="a3ccf-117">Per ottenere posizioni valide, usare il cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3ccf-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3ccf-118">-Name</span></span>
<span data-ttu-id="a3ccf-119">Specifica un nome per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="a3ccf-120">-Piano</span><span class="sxs-lookup"><span data-stu-id="a3ccf-120">-Plan</span></span>
<span data-ttu-id="a3ccf-121">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="a3ccf-122">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="a3ccf-122">Valid values are:</span></span>

- <span data-ttu-id="a3ccf-123">Base</span><span class="sxs-lookup"><span data-stu-id="a3ccf-123">Basic</span></span>
- <span data-ttu-id="a3ccf-124">Gratuito</span><span class="sxs-lookup"><span data-stu-id="a3ccf-124">Free</span></span>

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

### <span data-ttu-id="a3ccf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ccf-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3ccf-126">Specifica il nome di un gruppo di risorse a cui questo cmdlet aggiunge un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="a3ccf-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3ccf-127">-Tags</span></span>
<span data-ttu-id="a3ccf-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a3ccf-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="a3ccf-129">For example:</span></span>

<span data-ttu-id="a3ccf-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a3ccf-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a3ccf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ccf-131">CommonParameters</span></span>
<span data-ttu-id="a3ccf-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ccf-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ccf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ccf-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3ccf-134">INPUTS</span></span>

### <span data-ttu-id="a3ccf-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3ccf-135">None</span></span>
<span data-ttu-id="a3ccf-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a3ccf-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3ccf-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3ccf-137">OUTPUTS</span></span>

### <span data-ttu-id="a3ccf-138">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a3ccf-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="a3ccf-139">Note</span><span class="sxs-lookup"><span data-stu-id="a3ccf-139">NOTES</span></span>

## <span data-ttu-id="a3ccf-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3ccf-140">RELATED LINKS</span></span>

[<span data-ttu-id="a3ccf-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a3ccf-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="a3ccf-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a3ccf-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="a3ccf-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="a3ccf-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
