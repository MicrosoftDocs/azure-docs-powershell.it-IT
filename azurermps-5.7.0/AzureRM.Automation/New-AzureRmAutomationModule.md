---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685638"
---
# <span data-ttu-id="ac7b5-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ac7b5-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="ac7b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7b5-103">Importa un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac7b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac7b5-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac7b5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ac7b5-106">Il cmdlet **New-AzureRmAutomationModule** importa un modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="ac7b5-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="ac7b5-108">Il file contiene una cartella che include un file che è uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ac7b5-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="ac7b5-109">modulo wps_2, con estensione di file psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="ac7b5-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="ac7b5-110">wps_2 manifesto del modulo, con estensione psd1</span><span class="sxs-lookup"><span data-stu-id="ac7b5-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="ac7b5-111">Il nome del file zip, il nome della cartella e il nome del file nella cartella devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="ac7b5-112">Specificare il file zip come URL a cui può accedere il servizio di automazione.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="ac7b5-113">Se si importa un modulo di wps_2 in automazione tramite questo cmdlet o il cmdlet Set-AzureRmAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="ac7b5-114">Il comando termina se l'importazione ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="ac7b5-115">Per verificare se è riuscito, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="ac7b5-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="ac7b5-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="ac7b5-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="ac7b5-117">Controlla la proprietà **ProvisioningState** per un valore di succeeded.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="ac7b5-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac7b5-118">EXAMPLES</span></span>

### <span data-ttu-id="ac7b5-119">Esempio 1: importare un modulo</span><span class="sxs-lookup"><span data-stu-id="ac7b5-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ac7b5-120">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="ac7b5-121">Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="ac7b5-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac7b5-122">PARAMETERS</span></span>

### <span data-ttu-id="ac7b5-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ac7b5-123">-AutomationAccountName</span></span>
<span data-ttu-id="ac7b5-124">Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac7b5-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="ac7b5-125">-ContentLinkUri</span></span>
<span data-ttu-id="ac7b5-126">URL di un pacchetto zip di un modulo</span><span class="sxs-lookup"><span data-stu-id="ac7b5-126">The url to a module zip package</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac7b5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7b5-127">-DefaultProfile</span></span>
<span data-ttu-id="ac7b5-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ac7b5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac7b5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac7b5-129">-Name</span></span>
<span data-ttu-id="ac7b5-130">Specifica il nome del modulo importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-130">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="ac7b5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac7b5-131">-ResourceGroupName</span></span>
<span data-ttu-id="ac7b5-132">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-132">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="ac7b5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7b5-133">CommonParameters</span></span>
<span data-ttu-id="ac7b5-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7b5-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac7b5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7b5-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac7b5-136">INPUTS</span></span>

### <span data-ttu-id="ac7b5-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ac7b5-137">None</span></span>
<span data-ttu-id="ac7b5-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ac7b5-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ac7b5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac7b5-139">OUTPUTS</span></span>

### <span data-ttu-id="ac7b5-140">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="ac7b5-140">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="ac7b5-141">Note</span><span class="sxs-lookup"><span data-stu-id="ac7b5-141">NOTES</span></span>

## <span data-ttu-id="ac7b5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac7b5-142">RELATED LINKS</span></span>

[<span data-ttu-id="ac7b5-143">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ac7b5-143">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="ac7b5-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ac7b5-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="ac7b5-145">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="ac7b5-145">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


