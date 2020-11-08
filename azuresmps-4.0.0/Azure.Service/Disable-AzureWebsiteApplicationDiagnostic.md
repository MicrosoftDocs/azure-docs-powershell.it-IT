---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023648"
---
# <span data-ttu-id="5c182-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5c182-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="5c182-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c182-102">SYNOPSIS</span></span>
<span data-ttu-id="5c182-103">Disabilita la diagnostica delle applicazioni per un sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c182-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="5c182-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c182-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5c182-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c182-105">DESCRIPTION</span></span>
<span data-ttu-id="5c182-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c182-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5c182-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5c182-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5c182-108">Disabilita la diagnostica delle applicazioni per un sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c182-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="5c182-109">Disabilita la registrazione configurata per l'archiviazione in un file System o in Azure.</span><span class="sxs-lookup"><span data-stu-id="5c182-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="5c182-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c182-110">EXAMPLES</span></span>

### <span data-ttu-id="5c182-111">Esempio 1: disabilitare il file di registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5c182-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="5c182-112">L'esempio seguente disabilita la registrazione delle applicazioni nel file System.</span><span class="sxs-lookup"><span data-stu-id="5c182-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="5c182-113">Esempio 2: disabilitare la registrazione con l'archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="5c182-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="5c182-114">L'esempio seguente disabilita la registrazione delle applicazioni tramite lo spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5c182-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="5c182-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c182-115">PARAMETERS</span></span>

### <span data-ttu-id="5c182-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="5c182-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-117">-File</span><span class="sxs-lookup"><span data-stu-id="5c182-117">-File</span></span>
<span data-ttu-id="5c182-118">Specifica che si vuole usare il file System per archiviare i file di log.</span><span class="sxs-lookup"><span data-stu-id="5c182-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c182-119">-Name</span></span>
<span data-ttu-id="5c182-120">Specifica il nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="5c182-120">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c182-121">-PassThru</span></span>
<span data-ttu-id="5c182-122">Flag per restituire true se è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5c182-122">Flag to return true if succeeded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="5c182-123">-Profile</span></span>
<span data-ttu-id="5c182-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c182-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c182-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5c182-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c182-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="5c182-126">-Slot</span></span>
<span data-ttu-id="5c182-127">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="5c182-127">Specifies the name of slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="5c182-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c182-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c182-129">CommonParameters</span></span>
<span data-ttu-id="5c182-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c182-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c182-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c182-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c182-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c182-132">INPUTS</span></span>

## <span data-ttu-id="5c182-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c182-133">OUTPUTS</span></span>

## <span data-ttu-id="5c182-134">Note</span><span class="sxs-lookup"><span data-stu-id="5c182-134">NOTES</span></span>

## <span data-ttu-id="5c182-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c182-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c182-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5c182-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="5c182-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c182-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="5c182-138">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c182-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="5c182-139">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c182-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="5c182-140">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5c182-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


