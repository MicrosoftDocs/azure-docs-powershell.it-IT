---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029849"
---
# <span data-ttu-id="57c91-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="57c91-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="57c91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57c91-102">SYNOPSIS</span></span>
<span data-ttu-id="57c91-103">Crea i file e la configurazione necessari per un'applicazione PHP che verrà ospitata in Azure tramite php.exe.</span><span class="sxs-lookup"><span data-stu-id="57c91-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="57c91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57c91-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57c91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57c91-105">DESCRIPTION</span></span>
<span data-ttu-id="57c91-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57c91-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="57c91-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="57c91-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="57c91-108">Crea i file e la configurazione necessari, a volte definiti come ponteggi, per un'applicazione PHP che verrà ospitata in Azure tramite php.exe.</span><span class="sxs-lookup"><span data-stu-id="57c91-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="57c91-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57c91-109">EXAMPLES</span></span>

### <span data-ttu-id="57c91-110">Esempio 1: creare un ruolo di lavoro con una singola istanza</span><span class="sxs-lookup"><span data-stu-id="57c91-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="57c91-111">Questo esempio aggiunge i file e la configurazione necessari per un singolo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="57c91-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="57c91-112">Esempio 2: creare un ruolo di lavoro con più istanze</span><span class="sxs-lookup"><span data-stu-id="57c91-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="57c91-113">Questo esempio aggiunge i file e la configurazione necessari per un nuovo ruolo di lavoro all'applicazione corrente, usando il nome MyWorkerRole con un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="57c91-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="57c91-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57c91-114">PARAMETERS</span></span>

### <span data-ttu-id="57c91-115">-Istanze</span><span class="sxs-lookup"><span data-stu-id="57c91-115">-Instances</span></span>
<span data-ttu-id="57c91-116">Specifica il numero di istanze di ruolo per il ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="57c91-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="57c91-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="57c91-117">The default is 1.</span></span>

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

### <span data-ttu-id="57c91-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="57c91-118">-Name</span></span>
<span data-ttu-id="57c91-119">Specifica il nome del ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="57c91-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="57c91-120">Il nome determina il nome della cartella che contiene i file e la configurazione necessari per il servizio PHP ospitato nel ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="57c91-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="57c91-121">Il valore predefinito è WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="57c91-121">The default is WorkerRole1.</span></span>

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

### <span data-ttu-id="57c91-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="57c91-122">-Profile</span></span>
<span data-ttu-id="57c91-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c91-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57c91-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="57c91-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57c91-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c91-125">CommonParameters</span></span>
<span data-ttu-id="57c91-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c91-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c91-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c91-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c91-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57c91-128">INPUTS</span></span>

## <span data-ttu-id="57c91-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57c91-129">OUTPUTS</span></span>

## <span data-ttu-id="57c91-130">Note</span><span class="sxs-lookup"><span data-stu-id="57c91-130">NOTES</span></span>

## <span data-ttu-id="57c91-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57c91-131">RELATED LINKS</span></span>

[<span data-ttu-id="57c91-132">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="57c91-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="57c91-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="57c91-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


