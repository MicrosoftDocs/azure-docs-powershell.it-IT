---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029854"
---
# <span data-ttu-id="62a30-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="62a30-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="62a30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62a30-102">SYNOPSIS</span></span>
<span data-ttu-id="62a30-103">Crea file e cartelle necessari per un'applicazione di Node.js.</span><span class="sxs-lookup"><span data-stu-id="62a30-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="62a30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62a30-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="62a30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62a30-105">DESCRIPTION</span></span>
<span data-ttu-id="62a30-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="62a30-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="62a30-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="62a30-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="62a30-108">Il **componente aggiuntivo AzureNodeWebRole** crea file e cartelle necessari, a volte definiti come ponteggi, per un'applicazione Node.js ospitata nel cloud tramite IIS.</span><span class="sxs-lookup"><span data-stu-id="62a30-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="62a30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62a30-109">EXAMPLES</span></span>

### <span data-ttu-id="62a30-110">Esempio 1: ruolo Web istanza singola</span><span class="sxs-lookup"><span data-stu-id="62a30-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="62a30-111">Questo esempio aggiunge le impalcature per un singolo ruolo Web denominato **MyWebRole** all'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="62a30-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="62a30-112">Esempio 2: ruolo Web istanza multipla</span><span class="sxs-lookup"><span data-stu-id="62a30-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="62a30-113">Questo esempio aggiunge le impalcature per un nuovo ruolo Web denominato **MyWebRole** all'applicazione corrente, con un conteggio delle istanze del ruolo di 2.</span><span class="sxs-lookup"><span data-stu-id="62a30-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="62a30-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62a30-114">PARAMETERS</span></span>

### <span data-ttu-id="62a30-115">-Istanze</span><span class="sxs-lookup"><span data-stu-id="62a30-115">-Instances</span></span>
<span data-ttu-id="62a30-116">Specifica il numero di istanze di ruolo per questo ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="62a30-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="62a30-117">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="62a30-117">The default is 1.</span></span>

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

### <span data-ttu-id="62a30-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="62a30-118">-Name</span></span>
<span data-ttu-id="62a30-119">Specifica il nome del ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="62a30-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="62a30-120">Determina anche il nome della directory che contiene le impalcature per l'applicazione node.js che verranno ospitate nel ruolo Web.</span><span class="sxs-lookup"><span data-stu-id="62a30-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="62a30-121">Il valore predefinito è WebRole #, dove # indica il numero di ruoli Web nel servizio.</span><span class="sxs-lookup"><span data-stu-id="62a30-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="62a30-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="62a30-122">-Profile</span></span>
<span data-ttu-id="62a30-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a30-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="62a30-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="62a30-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="62a30-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a30-125">CommonParameters</span></span>
<span data-ttu-id="62a30-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a30-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a30-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a30-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a30-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62a30-128">INPUTS</span></span>

## <span data-ttu-id="62a30-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62a30-129">OUTPUTS</span></span>

## <span data-ttu-id="62a30-130">Note</span><span class="sxs-lookup"><span data-stu-id="62a30-130">NOTES</span></span>

## <span data-ttu-id="62a30-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62a30-131">RELATED LINKS</span></span>

[<span data-ttu-id="62a30-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="62a30-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="62a30-133">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="62a30-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


