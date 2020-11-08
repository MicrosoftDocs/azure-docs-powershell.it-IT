---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029685"
---
# <span data-ttu-id="24c4f-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="24c4f-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="24c4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24c4f-102">SYNOPSIS</span></span>

<span data-ttu-id="24c4f-103">Importa un modulo in automazione.</span><span class="sxs-lookup"><span data-stu-id="24c4f-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="24c4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24c4f-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="24c4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24c4f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="24c4f-106">Il cmdlet **New-AzureAutomationModule** importa un modulo in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="24c4f-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="24c4f-107">Un modulo è un file compresso con estensione zip che contiene una cartella che include uno dei tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="24c4f-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="24c4f-108">Modulo di Windows PowerShell (file psm1).</span><span class="sxs-lookup"><span data-stu-id="24c4f-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="24c4f-109">Un manifesto del modulo di Windows PowerShell (file psd1).</span><span class="sxs-lookup"><span data-stu-id="24c4f-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="24c4f-110">Un assembly (file dll).</span><span class="sxs-lookup"><span data-stu-id="24c4f-110">An assembly (dll file).</span></span>

<span data-ttu-id="24c4f-111">I nomi del file zip, la cartella nel file zip e il file nella cartella (con estensione psm1, PSD. 1 o. dll) devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="24c4f-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="24c4f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24c4f-112">EXAMPLES</span></span>

### <span data-ttu-id="24c4f-113">Esempio 1: importare un modulo</span><span class="sxs-lookup"><span data-stu-id="24c4f-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="24c4f-114">Questo comando importa un modulo denominato ContosoModule nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="24c4f-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="24c4f-115">Il modulo è archiviato in un BLOB di Azure in un account di archiviazione denominato contosostorage e un contenitore denominato modules.</span><span class="sxs-lookup"><span data-stu-id="24c4f-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="24c4f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24c4f-116">PARAMETERS</span></span>

### <span data-ttu-id="24c4f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24c4f-117">-AutomationAccountName</span></span>
<span data-ttu-id="24c4f-118">Specifica il nome dell'account di automazione in cui verrà archiviato il modulo.</span><span class="sxs-lookup"><span data-stu-id="24c4f-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4f-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="24c4f-119">-ContentLink</span></span>
<span data-ttu-id="24c4f-120">URL pubblico, ad esempio un sito Web o uno spazio di archiviazione BLOB di Azure che specifica il percorso del file del modulo.</span><span class="sxs-lookup"><span data-stu-id="24c4f-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="24c4f-121">Questa posizione deve essere accessibile pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="24c4f-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="24c4f-122">-Name</span></span>
<span data-ttu-id="24c4f-123">Specifica un nome per il modulo.</span><span class="sxs-lookup"><span data-stu-id="24c4f-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c4f-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="24c4f-124">-Profile</span></span>
<span data-ttu-id="24c4f-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24c4f-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24c4f-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="24c4f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c4f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="24c4f-127">-Tags</span></span>
<span data-ttu-id="24c4f-128">Specifica uno o più tag correlati al modulo.</span><span class="sxs-lookup"><span data-stu-id="24c4f-128">Specifies one or more tags related to the module.</span></span>

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

### <span data-ttu-id="24c4f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c4f-129">CommonParameters</span></span>
<span data-ttu-id="24c4f-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24c4f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c4f-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c4f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c4f-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24c4f-132">INPUTS</span></span>

## <span data-ttu-id="24c4f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24c4f-133">OUTPUTS</span></span>

### <span data-ttu-id="24c4f-134">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="24c4f-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="24c4f-135">Note</span><span class="sxs-lookup"><span data-stu-id="24c4f-135">NOTES</span></span>

## <span data-ttu-id="24c4f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24c4f-136">RELATED LINKS</span></span>

[<span data-ttu-id="24c4f-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="24c4f-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="24c4f-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="24c4f-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="24c4f-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="24c4f-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


