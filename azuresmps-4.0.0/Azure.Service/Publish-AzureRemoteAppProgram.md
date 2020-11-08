---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023842"
---
# <span data-ttu-id="439b2-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="439b2-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="439b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="439b2-102">SYNOPSIS</span></span>
<span data-ttu-id="439b2-103">Pubblica un programma RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="439b2-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="439b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="439b2-104">SYNTAX</span></span>

### <span data-ttu-id="439b2-105">ID app (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="439b2-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="439b2-106">Percorso dell'app</span><span class="sxs-lookup"><span data-stu-id="439b2-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="439b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="439b2-107">DESCRIPTION</span></span>
<span data-ttu-id="439b2-108">Il cmdlet **Publish-AzureRemoteAppProgram** pubblica un programma RemoteApp di Azure, che lo rende disponibile per gli utenti della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="439b2-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="439b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="439b2-109">EXAMPLES</span></span>

### <span data-ttu-id="439b2-110">Esempio 1: pubblicare un programma in una raccolta</span><span class="sxs-lookup"><span data-stu-id="439b2-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="439b2-111">Questo comando pubblica il programma nella raccolta ContosoApps con il *StartMenuAppId* specificato per aggiungere il programma al menu Start.</span><span class="sxs-lookup"><span data-stu-id="439b2-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="439b2-112">L'app pubblicata avrà un nome visualizzato "App Finanza".</span><span class="sxs-lookup"><span data-stu-id="439b2-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="439b2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="439b2-113">PARAMETERS</span></span>

### <span data-ttu-id="439b2-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="439b2-114">-CollectionName</span></span>
<span data-ttu-id="439b2-115">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="439b2-115">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439b2-116">-Riga di comando</span><span class="sxs-lookup"><span data-stu-id="439b2-116">-CommandLine</span></span>
<span data-ttu-id="439b2-117">Specifica gli argomenti della riga di comando per il programma pubblicato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439b2-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439b2-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="439b2-118">-DisplayName</span></span>
<span data-ttu-id="439b2-119">Specifica il nome visualizzato User-friendly del programma RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="439b2-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="439b2-120">Gli utenti lo vedono come il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="439b2-120">Users see this as the name of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439b2-121">-Filevirtualpath</span><span class="sxs-lookup"><span data-stu-id="439b2-121">-FileVirtualPath</span></span>
<span data-ttu-id="439b2-122">Specifica il percorso del programma nell'immagine del modello del programma.</span><span class="sxs-lookup"><span data-stu-id="439b2-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439b2-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="439b2-123">-Profile</span></span>
<span data-ttu-id="439b2-124">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439b2-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="439b2-125">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="439b2-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="439b2-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="439b2-126">-StartMenuAppId</span></span>
<span data-ttu-id="439b2-127">Specifica un GUID usato da questo cmdlet per aggiungere il programma al menu Start.</span><span class="sxs-lookup"><span data-stu-id="439b2-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439b2-128">CommonParameters</span></span>
<span data-ttu-id="439b2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439b2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439b2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="439b2-131">INPUTS</span></span>

## <span data-ttu-id="439b2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="439b2-132">OUTPUTS</span></span>

## <span data-ttu-id="439b2-133">Note</span><span class="sxs-lookup"><span data-stu-id="439b2-133">NOTES</span></span>

## <span data-ttu-id="439b2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="439b2-134">RELATED LINKS</span></span>

[<span data-ttu-id="439b2-135">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="439b2-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="439b2-136">Annulla pubblicazione-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="439b2-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


