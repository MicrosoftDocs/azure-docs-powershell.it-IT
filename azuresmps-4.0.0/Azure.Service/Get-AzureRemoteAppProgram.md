---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029781"
---
# <span data-ttu-id="00d8b-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="00d8b-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="00d8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="00d8b-103">Recupera le proprietà di una o più applicazioni di Azure RemoteApp pubblicate per una raccolta.</span><span class="sxs-lookup"><span data-stu-id="00d8b-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="00d8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00d8b-104">SYNTAX</span></span>

### <span data-ttu-id="00d8b-105">FilterByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00d8b-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="00d8b-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="00d8b-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="00d8b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00d8b-107">DESCRIPTION</span></span>
<span data-ttu-id="00d8b-108">Il cmdlet **Get-AzureRemoteAppProgram** recupera le proprietà di una o più applicazioni RemoteApp di Azure pubblicate per una raccolta.</span><span class="sxs-lookup"><span data-stu-id="00d8b-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="00d8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00d8b-109">EXAMPLES</span></span>

### <span data-ttu-id="00d8b-110">Esempio 1: recuperare le proprietà di un programma</span><span class="sxs-lookup"><span data-stu-id="00d8b-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="00d8b-111">Questo comando Visualizza le proprietà di un programma RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="00d8b-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="00d8b-112">Il programma, denominato app Finance, si trova nella raccolta RemoteApp di Azure denominata ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="00d8b-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="00d8b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00d8b-113">PARAMETERS</span></span>

### <span data-ttu-id="00d8b-114">-Alias</span><span class="sxs-lookup"><span data-stu-id="00d8b-114">-Alias</span></span>
<span data-ttu-id="00d8b-115">Specifica l'alias del programma per cui recuperare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="00d8b-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d8b-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="00d8b-116">-CollectionName</span></span>
<span data-ttu-id="00d8b-117">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="00d8b-117">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="00d8b-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="00d8b-118">-Profile</span></span>
<span data-ttu-id="00d8b-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d8b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00d8b-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="00d8b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00d8b-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="00d8b-121">-RemoteAppProgram</span></span>
<span data-ttu-id="00d8b-122">Specifica il nome del programma per cui recuperare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="00d8b-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="00d8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d8b-123">CommonParameters</span></span>
<span data-ttu-id="00d8b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d8b-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d8b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d8b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00d8b-126">INPUTS</span></span>

## <span data-ttu-id="00d8b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00d8b-127">OUTPUTS</span></span>

## <span data-ttu-id="00d8b-128">Note</span><span class="sxs-lookup"><span data-stu-id="00d8b-128">NOTES</span></span>

## <span data-ttu-id="00d8b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00d8b-129">RELATED LINKS</span></span>

[<span data-ttu-id="00d8b-130">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="00d8b-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="00d8b-131">Annulla pubblicazione-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="00d8b-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


