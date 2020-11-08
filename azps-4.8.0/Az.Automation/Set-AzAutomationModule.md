---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031975"
---
# <span data-ttu-id="c15a5-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c15a5-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="c15a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c15a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c15a5-103">Aggiorna un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="c15a5-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="c15a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c15a5-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c15a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c15a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c15a5-106">Il cmdlet **set-AzAutomationModule** aggiorna un modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c15a5-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="c15a5-107">Questo comando accetta un file compresso con estensione zip.</span><span class="sxs-lookup"><span data-stu-id="c15a5-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="c15a5-108">Il file contiene una cartella che include un file che è uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c15a5-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="c15a5-109">modulo wps_2, con estensione di file psm1 o dll</span><span class="sxs-lookup"><span data-stu-id="c15a5-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="c15a5-110">wps_2 manifesto del modulo, con estensione psd1, il nome del file zip, il nome della cartella e il nome del file nella cartella devono essere identici.</span><span class="sxs-lookup"><span data-stu-id="c15a5-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="c15a5-111">Specificare il file zip come URL a cui può accedere il servizio di automazione.</span><span class="sxs-lookup"><span data-stu-id="c15a5-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="c15a5-112">Se si importa un modulo di wps_2 in automazione tramite questo cmdlet o il cmdlet New-AzAutomationModule, l'operazione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="c15a5-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="c15a5-113">Il comando termina se l'importazione ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="c15a5-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="c15a5-114">Per verificare se è riuscito, eseguire il comando seguente: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName verificare la proprietà **ProvisioningState** per un valore di succeeded.</span><span class="sxs-lookup"><span data-stu-id="c15a5-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="c15a5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c15a5-115">EXAMPLES</span></span>

### <span data-ttu-id="c15a5-116">Esempio 1: aggiornare un modulo</span><span class="sxs-lookup"><span data-stu-id="c15a5-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c15a5-117">Questo comando importa una versione aggiornata di un modulo esistente denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c15a5-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="c15a5-118">Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="c15a5-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="c15a5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c15a5-119">PARAMETERS</span></span>

### <span data-ttu-id="c15a5-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c15a5-120">-AutomationAccountName</span></span>
<span data-ttu-id="c15a5-121">Specifica il nome dell'account di automazione per il quale questo cmdlet aggiorna un modulo.</span><span class="sxs-lookup"><span data-stu-id="c15a5-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c15a5-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="c15a5-122">-ContentLinkUri</span></span>
<span data-ttu-id="c15a5-123">Specifica l'URL del file con estensione zip che contiene la nuova versione di un modulo importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15a5-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15a5-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="c15a5-124">-ContentLinkVersion</span></span>
<span data-ttu-id="c15a5-125">Specifica la versione del modulo a cui questo cmdlet aggiorna l'automazione.</span><span class="sxs-lookup"><span data-stu-id="c15a5-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15a5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15a5-126">-DefaultProfile</span></span>
<span data-ttu-id="c15a5-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c15a5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c15a5-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c15a5-128">-Name</span></span>
<span data-ttu-id="c15a5-129">Specifica il nome del modulo importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c15a5-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c15a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c15a5-130">-ResourceGroupName</span></span>
<span data-ttu-id="c15a5-131">Specifica il nome di un gruppo di risorse per cui questo cmdlet aggiorna un modulo.</span><span class="sxs-lookup"><span data-stu-id="c15a5-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c15a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15a5-132">CommonParameters</span></span>
<span data-ttu-id="c15a5-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15a5-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15a5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15a5-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c15a5-135">INPUTS</span></span>

### <span data-ttu-id="c15a5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c15a5-136">System.String</span></span>

### <span data-ttu-id="c15a5-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="c15a5-137">System.Uri</span></span>

## <span data-ttu-id="c15a5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c15a5-138">OUTPUTS</span></span>

### <span data-ttu-id="c15a5-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="c15a5-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="c15a5-140">Note</span><span class="sxs-lookup"><span data-stu-id="c15a5-140">NOTES</span></span>

## <span data-ttu-id="c15a5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c15a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="c15a5-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c15a5-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="c15a5-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c15a5-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c15a5-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c15a5-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


