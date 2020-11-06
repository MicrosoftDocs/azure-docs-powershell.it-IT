---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521998"
---
# <span data-ttu-id="05d6a-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05d6a-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="05d6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="05d6a-103">Importa un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="05d6a-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05d6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05d6a-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05d6a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="05d6a-106">Il cmdlet **New-AzureRmAutomationModule** importa un modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="05d6a-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="05d6a-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="05d6a-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="05d6a-108">Il file contiene una cartella che include un file che è uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="05d6a-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="05d6a-109">modulo wps_2, con estensione di file psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="05d6a-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="05d6a-110">wps_2 manifesto del modulo, con estensione psd1</span><span class="sxs-lookup"><span data-stu-id="05d6a-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="05d6a-111">Il nome del file zip, il nome della cartella e il nome del file nella cartella devono essere uguali.</span><span class="sxs-lookup"><span data-stu-id="05d6a-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="05d6a-112">Specificare il file zip come URL a cui può accedere il servizio di automazione.</span><span class="sxs-lookup"><span data-stu-id="05d6a-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="05d6a-113">Se si importa un modulo di wps_2 in automazione tramite questo cmdlet o il cmdlet Set-AzureRmAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="05d6a-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="05d6a-114">Il comando termina se l'importazione ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="05d6a-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="05d6a-115">Per verificare se è riuscito, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="05d6a-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="05d6a-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="05d6a-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="05d6a-117">Controlla la proprietà **ProvisioningState** per un valore di succeeded.</span><span class="sxs-lookup"><span data-stu-id="05d6a-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="05d6a-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05d6a-118">EXAMPLES</span></span>

### <span data-ttu-id="05d6a-119">Esempio 1: importare un modulo</span><span class="sxs-lookup"><span data-stu-id="05d6a-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05d6a-120">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="05d6a-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="05d6a-121">Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="05d6a-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="05d6a-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05d6a-122">PARAMETERS</span></span>

### <span data-ttu-id="05d6a-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05d6a-123">-AutomationAccountName</span></span>
<span data-ttu-id="05d6a-124">Specifica il nome dell'account di automazione per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="05d6a-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="05d6a-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="05d6a-125">-ContentLinkUri</span></span>
<span data-ttu-id="05d6a-126">L'URL di un pacchetto zip del modulo.</span><span class="sxs-lookup"><span data-stu-id="05d6a-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05d6a-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="05d6a-127">-Name</span></span>
<span data-ttu-id="05d6a-128">Specifica il nome del modulo importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05d6a-128">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="05d6a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d6a-129">-ResourceGroupName</span></span>
<span data-ttu-id="05d6a-130">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa un modulo.</span><span class="sxs-lookup"><span data-stu-id="05d6a-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="05d6a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d6a-131">-DefaultProfile</span></span>
<span data-ttu-id="05d6a-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05d6a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d6a-133">CommonParameters</span></span>
<span data-ttu-id="05d6a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d6a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d6a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d6a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05d6a-136">INPUTS</span></span>

## <span data-ttu-id="05d6a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05d6a-137">OUTPUTS</span></span>

### <span data-ttu-id="05d6a-138">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="05d6a-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="05d6a-139">Note</span><span class="sxs-lookup"><span data-stu-id="05d6a-139">NOTES</span></span>

## <span data-ttu-id="05d6a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05d6a-140">RELATED LINKS</span></span>

[<span data-ttu-id="05d6a-141">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05d6a-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="05d6a-142">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05d6a-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="05d6a-143">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="05d6a-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


