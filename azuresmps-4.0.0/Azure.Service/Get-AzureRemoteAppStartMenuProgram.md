---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029777"
---
# <span data-ttu-id="a7323-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="a7323-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="a7323-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7323-102">SYNOPSIS</span></span>
<span data-ttu-id="a7323-103">Elenca i programmi del menu Start in una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7323-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a7323-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7323-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7323-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7323-105">DESCRIPTION</span></span>
<span data-ttu-id="a7323-106">Il cmdlet **Get-AzureRemoteAppStartMenuProgram** elenca i programmi del menu Start nell'immagine del modello utilizzata da una raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7323-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="a7323-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7323-107">EXAMPLES</span></span>

### <span data-ttu-id="a7323-108">Esempio 1: elencare le applicazioni del menu Start per una raccolta</span><span class="sxs-lookup"><span data-stu-id="a7323-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="a7323-109">Questo comando restituisce l'elenco dei programmi di menu Start per la raccolta ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="a7323-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="a7323-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7323-110">PARAMETERS</span></span>

### <span data-ttu-id="a7323-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a7323-111">-CollectionName</span></span>
<span data-ttu-id="a7323-112">Specifica il nome della raccolta RemoteApp di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7323-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="a7323-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a7323-113">-Profile</span></span>
<span data-ttu-id="a7323-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7323-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7323-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a7323-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7323-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="a7323-116">-ProgramName</span></span>
<span data-ttu-id="a7323-117">Specifica il nome di un programma per cui elencare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7323-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="a7323-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7323-118">CommonParameters</span></span>
<span data-ttu-id="a7323-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7323-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7323-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7323-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7323-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7323-121">INPUTS</span></span>

## <span data-ttu-id="a7323-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7323-122">OUTPUTS</span></span>

## <span data-ttu-id="a7323-123">Note</span><span class="sxs-lookup"><span data-stu-id="a7323-123">NOTES</span></span>

## <span data-ttu-id="a7323-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7323-124">RELATED LINKS</span></span>

[<span data-ttu-id="a7323-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="a7323-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


