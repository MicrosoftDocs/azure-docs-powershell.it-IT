---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012733"
---
# <span data-ttu-id="a92fd-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a92fd-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="a92fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a92fd-103">Importa un modulo nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="a92fd-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="a92fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a92fd-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92fd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a92fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a92fd-106">Il cmdlet **New-AzAutomationModule** importa un modulo nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a92fd-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="a92fd-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="a92fd-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="a92fd-108">Il file contiene una cartella che include un file di uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a92fd-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="a92fd-109">Windows PowerShell modulo, con estensione psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="a92fd-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="a92fd-110">Windows PowerShell manifesto del modulo, con estensione psd1, il nome del file ZIP, il nome della cartella e il nome del file nella cartella devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="a92fd-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="a92fd-111">Specificare il file ZIP come URL a cui il servizio di automazione può accedere.</span><span class="sxs-lookup"><span data-stu-id="a92fd-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="a92fd-112">Se si importa un modulo Windows PowerShell'automazione usando questo cmdlet o il cmdlet Set-AzAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="a92fd-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="a92fd-113">Il comando termina se l'importazione riesce o meno.</span><span class="sxs-lookup"><span data-stu-id="a92fd-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="a92fd-114">Per verificare se l'operazione ha avuto esito positivo, eseguire il comando seguente: ModuleName Controllare la proprietà ProvisioningState per il valore `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Succeeded. </span><span class="sxs-lookup"><span data-stu-id="a92fd-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="a92fd-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a92fd-115">EXAMPLES</span></span>

### <span data-ttu-id="a92fd-116">Esempio 1: Importare un modulo</span><span class="sxs-lookup"><span data-stu-id="a92fd-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a92fd-117">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a92fd-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="a92fd-118">Il modulo viene archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e in un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="a92fd-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="a92fd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a92fd-119">PARAMETERS</span></span>

### <span data-ttu-id="a92fd-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a92fd-120">-AutomationAccountName</span></span>
<span data-ttu-id="a92fd-121">Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="a92fd-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="a92fd-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="a92fd-122">-ContentLinkUri</span></span>
<span data-ttu-id="a92fd-123">URL di un pacchetto ZIP del modulo</span><span class="sxs-lookup"><span data-stu-id="a92fd-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="a92fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92fd-124">-DefaultProfile</span></span>
<span data-ttu-id="a92fd-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a92fd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92fd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a92fd-126">-Name</span></span>
<span data-ttu-id="a92fd-127">Specifica il nome del modulo che questo cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="a92fd-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="a92fd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92fd-128">-ResourceGroupName</span></span>
<span data-ttu-id="a92fd-129">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="a92fd-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="a92fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92fd-130">CommonParameters</span></span>
<span data-ttu-id="a92fd-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92fd-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92fd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92fd-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a92fd-133">INPUTS</span></span>

### <span data-ttu-id="a92fd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a92fd-134">System.String</span></span>

### <span data-ttu-id="a92fd-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="a92fd-135">System.Uri</span></span>

## <span data-ttu-id="a92fd-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a92fd-136">OUTPUTS</span></span>

### <span data-ttu-id="a92fd-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="a92fd-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="a92fd-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="a92fd-138">NOTES</span></span>

## <span data-ttu-id="a92fd-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a92fd-139">RELATED LINKS</span></span>

[<span data-ttu-id="a92fd-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a92fd-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="a92fd-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a92fd-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="a92fd-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a92fd-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


