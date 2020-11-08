---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029968"
---
# <span data-ttu-id="34142-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="34142-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="34142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34142-102">SYNOPSIS</span></span>
<span data-ttu-id="34142-103">Ottiene i registri per il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="34142-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="34142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34142-104">SYNTAX</span></span>

### <span data-ttu-id="34142-105">Coda</span><span class="sxs-lookup"><span data-stu-id="34142-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34142-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="34142-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="34142-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34142-107">DESCRIPTION</span></span>
<span data-ttu-id="34142-108">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34142-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="34142-109">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="34142-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="34142-110">Ottiene il log per il sito Web specificato.</span><span class="sxs-lookup"><span data-stu-id="34142-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="34142-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34142-111">EXAMPLES</span></span>

### <span data-ttu-id="34142-112">Esempio 1: avviare il flusso di log</span><span class="sxs-lookup"><span data-stu-id="34142-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="34142-113">Questo esempio avvia il flusso di log per tutti i registri delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="34142-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="34142-114">Esempio 2: avviare il flusso di log per i registri http</span><span class="sxs-lookup"><span data-stu-id="34142-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="34142-115">Questo esempio avvia il flusso di log per i registri http.</span><span class="sxs-lookup"><span data-stu-id="34142-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="34142-116">Esempio 3: avviare il flusso di log per i log degli errori</span><span class="sxs-lookup"><span data-stu-id="34142-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="34142-117">Questo esempio avvia log streaming e Mostra solo i log degli errori.</span><span class="sxs-lookup"><span data-stu-id="34142-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="34142-118">Esempio 4: visualizzare i registri disponibili</span><span class="sxs-lookup"><span data-stu-id="34142-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="34142-119">Questo esempio elenca tutti i percorsi di log disponibili nel sito Web.</span><span class="sxs-lookup"><span data-stu-id="34142-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="34142-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34142-120">PARAMETERS</span></span>

### <span data-ttu-id="34142-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="34142-121">-ListPath</span></span>
<span data-ttu-id="34142-122">Indica se elencare i percorsi del log.</span><span class="sxs-lookup"><span data-stu-id="34142-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34142-123">-Messaggio</span><span class="sxs-lookup"><span data-stu-id="34142-123">-Message</span></span>
<span data-ttu-id="34142-124">Specifica una stringa che verrà usata per filtrare il messaggio di log.</span><span class="sxs-lookup"><span data-stu-id="34142-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="34142-125">Verranno recuperati solo i registri che contengono la stringa.</span><span class="sxs-lookup"><span data-stu-id="34142-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34142-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="34142-126">-Name</span></span>
<span data-ttu-id="34142-127">Nome del sito Web.</span><span class="sxs-lookup"><span data-stu-id="34142-127">The name of the website.</span></span>

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

### <span data-ttu-id="34142-128">-Path</span><span class="sxs-lookup"><span data-stu-id="34142-128">-Path</span></span>
<span data-ttu-id="34142-129">Percorso da cui verrà recuperato il log.</span><span class="sxs-lookup"><span data-stu-id="34142-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="34142-130">Per impostazione predefinita, è radice, ovvero include tutti i percorsi.</span><span class="sxs-lookup"><span data-stu-id="34142-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34142-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="34142-131">-Profile</span></span>
<span data-ttu-id="34142-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34142-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34142-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="34142-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34142-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="34142-134">-Slot</span></span>
<span data-ttu-id="34142-135">Specifica il nome dello slot.</span><span class="sxs-lookup"><span data-stu-id="34142-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="34142-136">-Coda</span><span class="sxs-lookup"><span data-stu-id="34142-136">-Tail</span></span>
<span data-ttu-id="34142-137">Specifica se eseguire il flusso dei log.</span><span class="sxs-lookup"><span data-stu-id="34142-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34142-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34142-138">CommonParameters</span></span>
<span data-ttu-id="34142-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34142-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34142-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34142-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34142-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34142-141">INPUTS</span></span>

## <span data-ttu-id="34142-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34142-142">OUTPUTS</span></span>

## <span data-ttu-id="34142-143">Note</span><span class="sxs-lookup"><span data-stu-id="34142-143">NOTES</span></span>

## <span data-ttu-id="34142-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34142-144">RELATED LINKS</span></span>

[<span data-ttu-id="34142-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="34142-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="34142-146">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="34142-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="34142-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="34142-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="34142-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="34142-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


