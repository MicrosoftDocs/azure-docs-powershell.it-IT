---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686346"
---
# <span data-ttu-id="b2751-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2751-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="b2751-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2751-102">SYNOPSIS</span></span>
<span data-ttu-id="b2751-103">Crea un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2751-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2751-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2751-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2751-105">DESCRIPTION</span></span>
<span data-ttu-id="b2751-106">Il cmdlet **New-AzureRmAutomationAccount** crea un account di automazione di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2751-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="b2751-107">Un account di automazione è un contenitore per le risorse di automazione che viene isolato dalle risorse di altri account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="b2751-108">Le risorse di automazione includono manuali operativi, configurazioni di configurazione dello stato (DSC) desiderate, processi e asset.</span><span class="sxs-lookup"><span data-stu-id="b2751-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="b2751-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2751-109">EXAMPLES</span></span>

### <span data-ttu-id="b2751-110">Esempio 1: creare un account di automazione</span><span class="sxs-lookup"><span data-stu-id="b2751-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b2751-111">Questo comando crea un nuovo account di automazione denominato ContosoAutomationAccount nell'area est degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="b2751-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="b2751-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2751-112">PARAMETERS</span></span>

### <span data-ttu-id="b2751-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b2751-113">-Location</span></span>
<span data-ttu-id="b2751-114">Specifica la posizione in cui questo cmdlet crea l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="b2751-115">Per ottenere posizioni valide, usare il cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="b2751-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="b2751-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2751-116">-Name</span></span>
<span data-ttu-id="b2751-117">Specifica un nome per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="b2751-118">-Piano</span><span class="sxs-lookup"><span data-stu-id="b2751-118">-Plan</span></span>
<span data-ttu-id="b2751-119">Specifica il piano per l'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="b2751-120">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b2751-120">Valid values are:</span></span>

- <span data-ttu-id="b2751-121">Base</span><span class="sxs-lookup"><span data-stu-id="b2751-121">Basic</span></span>
- <span data-ttu-id="b2751-122">Gratuito</span><span class="sxs-lookup"><span data-stu-id="b2751-122">Free</span></span>

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

### <span data-ttu-id="b2751-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2751-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2751-124">Specifica il nome di un gruppo di risorse a cui questo cmdlet aggiunge un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b2751-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="b2751-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2751-125">-Tags</span></span>
<span data-ttu-id="b2751-126">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b2751-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2751-127">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b2751-127">For example:</span></span>

<span data-ttu-id="b2751-128">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b2751-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2751-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2751-129">-DefaultProfile</span></span>
<span data-ttu-id="b2751-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2751-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2751-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2751-131">CommonParameters</span></span>
<span data-ttu-id="b2751-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2751-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2751-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2751-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2751-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2751-134">INPUTS</span></span>

## <span data-ttu-id="b2751-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2751-135">OUTPUTS</span></span>

### <span data-ttu-id="b2751-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2751-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="b2751-137">Note</span><span class="sxs-lookup"><span data-stu-id="b2751-137">NOTES</span></span>

## <span data-ttu-id="b2751-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2751-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2751-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2751-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="b2751-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2751-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="b2751-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="b2751-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
