---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029852"
---
# <span data-ttu-id="c34bd-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="c34bd-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="c34bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c34bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c34bd-103">Crea i file e la configurazione necessari per un'applicazione PHP.</span><span class="sxs-lookup"><span data-stu-id="c34bd-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="c34bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c34bd-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c34bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c34bd-105">DESCRIPTION</span></span>
<span data-ttu-id="c34bd-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c34bd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c34bd-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c34bd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c34bd-108">Il cmdlet **Add-AzurePHPWebRole** crea i file e la configurazione, a volte definiti ponteggi, per un'applicazione php che verrà ospitata in Azure tramite IIS.</span><span class="sxs-lookup"><span data-stu-id="c34bd-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="c34bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c34bd-109">EXAMPLES</span></span>

### <span data-ttu-id="c34bd-110">Esempio 1: aggiungere un ruolo Web usando i valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="c34bd-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="c34bd-111">Questo esempio aggiunge i file e la configurazione necessari per il nuovo ruolo Web usando i valori predefiniti di un servizio denominato "WebRole1" con 1 istanza.</span><span class="sxs-lookup"><span data-stu-id="c34bd-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="c34bd-112">Esempio 2: aggiungere un ruolo Web con più istanze</span><span class="sxs-lookup"><span data-stu-id="c34bd-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="c34bd-113">Questo esempio aggiunge i file e la configurazione necessari per un nuovo ruolo Web all'applicazione corrente, usando il nome "MyWebRole" e un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="c34bd-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="c34bd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c34bd-114">PARAMETERS</span></span>

### <span data-ttu-id="c34bd-115">-Istanze</span><span class="sxs-lookup"><span data-stu-id="c34bd-115">-Instances</span></span>
<span data-ttu-id="c34bd-116">Specifica il numero di istanze di ruolo per questo ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="c34bd-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="c34bd-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="c34bd-117">The default is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c34bd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c34bd-118">-Name</span></span>
<span data-ttu-id="c34bd-119">Specifica il nome del ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="c34bd-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="c34bd-120">Il nome determina il nome della directory che contiene i file e la configurazione necessari per l'applicazione PHP.</span><span class="sxs-lookup"><span data-stu-id="c34bd-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="c34bd-121">Il valore predefinito è WebRole #, dove # rappresenta il numero di ruoli Web nel servizio.</span><span class="sxs-lookup"><span data-stu-id="c34bd-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c34bd-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="c34bd-122">-Profile</span></span>
<span data-ttu-id="c34bd-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c34bd-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c34bd-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c34bd-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c34bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34bd-125">CommonParameters</span></span>
<span data-ttu-id="c34bd-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c34bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34bd-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34bd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34bd-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c34bd-128">INPUTS</span></span>

## <span data-ttu-id="c34bd-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c34bd-129">OUTPUTS</span></span>

## <span data-ttu-id="c34bd-130">Note</span><span class="sxs-lookup"><span data-stu-id="c34bd-130">NOTES</span></span>

## <span data-ttu-id="c34bd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c34bd-131">RELATED LINKS</span></span>

[<span data-ttu-id="c34bd-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="c34bd-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="c34bd-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="c34bd-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


