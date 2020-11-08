---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023668"
---
# <span data-ttu-id="ae1c8-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="ae1c8-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="ae1c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae1c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1c8-103">Crea i file e la configurazione necessari per un ruolo di lavoro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="ae1c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae1c8-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae1c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae1c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1c8-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ae1c8-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ae1c8-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ae1c8-108">Il cmdlet **Add-AzureWorkerRole** crea i file e la configurazione necessari, a volte definiti come ponteggi, per un ruolo di lavoro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="ae1c8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae1c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ae1c8-110">Esempio 1: creare un singolo ruolo di lavoro istanza</span><span class="sxs-lookup"><span data-stu-id="ae1c8-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="ae1c8-111">Questo esempio aggiunge le impalcature per un singolo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="ae1c8-112">Esempio 2: creare un ruolo di lavoro a più istanze</span><span class="sxs-lookup"><span data-stu-id="ae1c8-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="ae1c8-113">Questo esempio aggiunge le impalcature per un nuovo ruolo di lavoro denominato MyWorkerRole all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="ae1c8-114">Esempio 3: creare un ruolo di lavoro con le impalcature personalizzate</span><span class="sxs-lookup"><span data-stu-id="ae1c8-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="ae1c8-115">Questo esempio crea un ruolo di lavoro con un'impalcatura personalizzata.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="ae1c8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae1c8-116">PARAMETERS</span></span>

### <span data-ttu-id="ae1c8-117">-Istanze</span><span class="sxs-lookup"><span data-stu-id="ae1c8-117">-Instances</span></span>
<span data-ttu-id="ae1c8-118">Specifica il numero di istanze di ruolo per il ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="ae1c8-119">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-119">The default is 1.</span></span>

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

### <span data-ttu-id="ae1c8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae1c8-120">-Name</span></span>
<span data-ttu-id="ae1c8-121">Specifica il nome del ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="ae1c8-122">Questo valore determina il nome della cartella che contiene le impalcature per l'applicazione personalizzata che verranno ospitate nel ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="ae1c8-123">Il valore predefinito è WorkerRolenumber, dove numero è il numero di ruoli di lavoro nel servizio.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="ae1c8-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae1c8-124">-Profile</span></span>
<span data-ttu-id="ae1c8-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae1c8-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae1c8-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="ae1c8-127">-TemplateFolder</span></span>
<span data-ttu-id="ae1c8-128">Specifica la cartella del modello di ponteggi da usare per creare il ruolo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="ae1c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1c8-129">CommonParameters</span></span>
<span data-ttu-id="ae1c8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae1c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1c8-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1c8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1c8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae1c8-132">INPUTS</span></span>

## <span data-ttu-id="ae1c8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae1c8-133">OUTPUTS</span></span>

## <span data-ttu-id="ae1c8-134">Note</span><span class="sxs-lookup"><span data-stu-id="ae1c8-134">NOTES</span></span>

## <span data-ttu-id="ae1c8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae1c8-135">RELATED LINKS</span></span>

[<span data-ttu-id="ae1c8-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="ae1c8-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="ae1c8-137">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="ae1c8-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


