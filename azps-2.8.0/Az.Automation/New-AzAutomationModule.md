---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 7e9b2e9a87cc9a02c807a2eae3b64e7a13c87a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675757"
---
# <span data-ttu-id="17f84-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17f84-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="17f84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17f84-102">SYNOPSIS</span></span>
<span data-ttu-id="17f84-103">Importa un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="17f84-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="17f84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17f84-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17f84-105">DESCRIPTION</span></span>
<span data-ttu-id="17f84-106">Il cmdlet **New-AzAutomationModule** importa un modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="17f84-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="17f84-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="17f84-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="17f84-108">Il file contiene una cartella che include un file che è uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="17f84-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="17f84-109">Modulo di Windows PowerShell, con estensione di file psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="17f84-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="17f84-110">Manifesto del modulo di Windows PowerShell, con estensione psd1 il nome del file zip, il nome della cartella e il nome del file nella cartella devono essere identici.</span><span class="sxs-lookup"><span data-stu-id="17f84-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="17f84-111">Specificare il file zip come URL a cui può accedere il servizio di automazione.</span><span class="sxs-lookup"><span data-stu-id="17f84-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="17f84-112">Se si importa un modulo di Windows PowerShell in automazione usando questo cmdlet o il cmdlet Set-AzAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="17f84-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="17f84-113">Il comando termina se l'importazione ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="17f84-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="17f84-114">Per verificare se è riuscito, eseguire il comando seguente: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName verificare la proprietà **ProvisioningState** per un valore di succeeded.</span><span class="sxs-lookup"><span data-stu-id="17f84-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="17f84-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17f84-115">EXAMPLES</span></span>

### <span data-ttu-id="17f84-116">Esempio 1: importare un modulo</span><span class="sxs-lookup"><span data-stu-id="17f84-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="17f84-117">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="17f84-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="17f84-118">Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="17f84-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="17f84-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17f84-119">PARAMETERS</span></span>

### <span data-ttu-id="17f84-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="17f84-120">-AutomationAccountName</span></span>
<span data-ttu-id="17f84-121">Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="17f84-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="17f84-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="17f84-122">-ContentLinkUri</span></span>
<span data-ttu-id="17f84-123">URL di un pacchetto zip di un modulo</span><span class="sxs-lookup"><span data-stu-id="17f84-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="17f84-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f84-124">-DefaultProfile</span></span>
<span data-ttu-id="17f84-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="17f84-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17f84-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="17f84-126">-Name</span></span>
<span data-ttu-id="17f84-127">Specifica il nome del modulo importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17f84-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="17f84-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f84-128">-ResourceGroupName</span></span>
<span data-ttu-id="17f84-129">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="17f84-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="17f84-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f84-130">CommonParameters</span></span>
<span data-ttu-id="17f84-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f84-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f84-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f84-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f84-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17f84-133">INPUTS</span></span>

### <span data-ttu-id="17f84-134">System. String</span><span class="sxs-lookup"><span data-stu-id="17f84-134">System.String</span></span>

### <span data-ttu-id="17f84-135">System. Uri</span><span class="sxs-lookup"><span data-stu-id="17f84-135">System.Uri</span></span>

## <span data-ttu-id="17f84-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17f84-136">OUTPUTS</span></span>

### <span data-ttu-id="17f84-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="17f84-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="17f84-138">Note</span><span class="sxs-lookup"><span data-stu-id="17f84-138">NOTES</span></span>

## <span data-ttu-id="17f84-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17f84-139">RELATED LINKS</span></span>

[<span data-ttu-id="17f84-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17f84-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="17f84-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17f84-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="17f84-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="17f84-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)

