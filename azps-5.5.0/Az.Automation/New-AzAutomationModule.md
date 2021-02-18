---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201063"
---
# <span data-ttu-id="4ecbd-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ecbd-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="4ecbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ecbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecbd-103">Importa un modulo nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="4ecbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ecbd-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecbd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ecbd-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecbd-106">Il cmdlet **New-AzAutomationModule** importa un modulo nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="4ecbd-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="4ecbd-108">Il file contiene una cartella che include un file di uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ecbd-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="4ecbd-109">Windows PowerShell modulo, con estensione psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="4ecbd-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="4ecbd-110">Windows PowerShell manifesto del modulo, con estensione psd1, Il nome del file ZIP, il nome della cartella e il nome del file nella cartella devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="4ecbd-111">Specificare il file ZIP come URL a cui il servizio di automazione può accedere.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="4ecbd-112">Se si importa un modulo Windows PowerShell'automazione usando questo cmdlet o il cmdlet Set-AzAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="4ecbd-113">Il comando termina se l'importazione riesce o meno.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="4ecbd-114">Per verificare se l'operazione ha avuto esito positivo, eseguire il comando seguente: ModuleName Controllare la proprietà ProvisioningState per il valore `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Succeeded. </span><span class="sxs-lookup"><span data-stu-id="4ecbd-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="4ecbd-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ecbd-115">EXAMPLES</span></span>

### <span data-ttu-id="4ecbd-116">Esempio 1: Importare un modulo</span><span class="sxs-lookup"><span data-stu-id="4ecbd-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4ecbd-117">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="4ecbd-118">Il modulo viene archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e in un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="4ecbd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ecbd-119">PARAMETERS</span></span>

### <span data-ttu-id="4ecbd-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ecbd-120">-AutomationAccountName</span></span>
<span data-ttu-id="4ecbd-121">Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="4ecbd-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="4ecbd-122">-ContentLinkUri</span></span>
<span data-ttu-id="4ecbd-123">URL di un pacchetto ZIP del modulo</span><span class="sxs-lookup"><span data-stu-id="4ecbd-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecbd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecbd-124">-DefaultProfile</span></span>
<span data-ttu-id="4ecbd-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4ecbd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ecbd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4ecbd-126">-Name</span></span>
<span data-ttu-id="4ecbd-127">Specifica il nome del modulo che questo cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="4ecbd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecbd-128">-ResourceGroupName</span></span>
<span data-ttu-id="4ecbd-129">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="4ecbd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecbd-130">CommonParameters</span></span>
<span data-ttu-id="4ecbd-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecbd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecbd-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecbd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecbd-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ecbd-133">INPUTS</span></span>

### <span data-ttu-id="4ecbd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4ecbd-134">System.String</span></span>

### <span data-ttu-id="4ecbd-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="4ecbd-135">System.Uri</span></span>

## <span data-ttu-id="4ecbd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ecbd-136">OUTPUTS</span></span>

### <span data-ttu-id="4ecbd-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="4ecbd-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4ecbd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ecbd-138">NOTES</span></span>

## <span data-ttu-id="4ecbd-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ecbd-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ecbd-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ecbd-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="4ecbd-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ecbd-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="4ecbd-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ecbd-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


