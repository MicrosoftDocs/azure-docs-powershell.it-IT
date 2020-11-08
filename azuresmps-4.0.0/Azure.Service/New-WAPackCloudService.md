---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030819"
---
# <span data-ttu-id="2dc03-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="2dc03-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="2dc03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dc03-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc03-103">Crea un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2dc03-103">Creates a cloud service.</span></span>

## <span data-ttu-id="2dc03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dc03-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2dc03-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dc03-105">DESCRIPTION</span></span>
<span data-ttu-id="2dc03-106">Questi argomenti sono deprecati e verranno rimossi in futuro.</span><span class="sxs-lookup"><span data-stu-id="2dc03-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="2dc03-107">Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc03-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2dc03-108">Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2dc03-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2dc03-109">Il cmdlet **New-WAPackCloudService** crea un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2dc03-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="2dc03-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dc03-110">EXAMPLES</span></span>

### <span data-ttu-id="2dc03-111">Esempio 1: creare un servizio cloud</span><span class="sxs-lookup"><span data-stu-id="2dc03-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="2dc03-112">Il comando crea un servizio cloud denominato ContosoCloudService01 con un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="2dc03-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="2dc03-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dc03-113">PARAMETERS</span></span>

### <span data-ttu-id="2dc03-114">-Etichetta</span><span class="sxs-lookup"><span data-stu-id="2dc03-114">-Label</span></span>
<span data-ttu-id="2dc03-115">Specifica un'etichetta per il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="2dc03-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="2dc03-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dc03-116">-Name</span></span>
<span data-ttu-id="2dc03-117">Specifica un nome per cloudservice.</span><span class="sxs-lookup"><span data-stu-id="2dc03-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="2dc03-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="2dc03-118">-Profile</span></span>
<span data-ttu-id="2dc03-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc03-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2dc03-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2dc03-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2dc03-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc03-121">CommonParameters</span></span>
<span data-ttu-id="2dc03-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc03-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc03-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dc03-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc03-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dc03-124">INPUTS</span></span>

## <span data-ttu-id="2dc03-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dc03-125">OUTPUTS</span></span>

## <span data-ttu-id="2dc03-126">Note</span><span class="sxs-lookup"><span data-stu-id="2dc03-126">NOTES</span></span>

## <span data-ttu-id="2dc03-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dc03-127">RELATED LINKS</span></span>

[<span data-ttu-id="2dc03-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="2dc03-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="2dc03-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="2dc03-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


