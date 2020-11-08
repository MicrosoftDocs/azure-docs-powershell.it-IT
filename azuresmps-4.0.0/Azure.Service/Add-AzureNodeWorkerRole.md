---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029851"
---
# <span data-ttu-id="51bea-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="51bea-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="51bea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51bea-102">SYNOPSIS</span></span>
<span data-ttu-id="51bea-103">Crea i file e le cartelle necessari per un'applicazione di Node.js ospitata nel cloud tramite node.exe</span><span class="sxs-lookup"><span data-stu-id="51bea-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="51bea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51bea-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="51bea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51bea-105">DESCRIPTION</span></span>
<span data-ttu-id="51bea-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="51bea-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="51bea-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="51bea-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="51bea-108">Il cmdlet **Add-AzureNodeWorkerRole** crea i file e le cartelle necessari, a volte definiti come ponteggi, perché un'applicazione Node.js sia ospitata nel cloud tramite node.exe.</span><span class="sxs-lookup"><span data-stu-id="51bea-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="51bea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51bea-109">EXAMPLES</span></span>

### <span data-ttu-id="51bea-110">Esempio 1: ruolo di lavoratore a istanza singola</span><span class="sxs-lookup"><span data-stu-id="51bea-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="51bea-111">Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato **MyWorkerRole** all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="51bea-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="51bea-112">Esempio 2: ruolo di lavoro più istanze</span><span class="sxs-lookup"><span data-stu-id="51bea-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="51bea-113">Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato **MyWorkerRole** all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="51bea-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="51bea-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51bea-114">PARAMETERS</span></span>

### <span data-ttu-id="51bea-115">-Istanze</span><span class="sxs-lookup"><span data-stu-id="51bea-115">-Instances</span></span>
<span data-ttu-id="51bea-116">Specifica il numero di istanze di ruolo per il ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="51bea-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="51bea-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="51bea-117">Default is 1.</span></span>

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

### <span data-ttu-id="51bea-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="51bea-118">-Name</span></span>
<span data-ttu-id="51bea-119">Specifica il nome del ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="51bea-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="51bea-120">Il valore determina il nome della cartella che contiene le impalcature per il servizio di node.js ospitate nel ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="51bea-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="51bea-121">Il valore predefinito è WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="51bea-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="51bea-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="51bea-122">-Profile</span></span>
<span data-ttu-id="51bea-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51bea-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51bea-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="51bea-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="51bea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bea-125">CommonParameters</span></span>
<span data-ttu-id="51bea-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bea-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bea-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51bea-128">INPUTS</span></span>

## <span data-ttu-id="51bea-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51bea-129">OUTPUTS</span></span>

## <span data-ttu-id="51bea-130">Note</span><span class="sxs-lookup"><span data-stu-id="51bea-130">NOTES</span></span>

## <span data-ttu-id="51bea-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51bea-131">RELATED LINKS</span></span>

[<span data-ttu-id="51bea-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="51bea-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="51bea-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="51bea-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


