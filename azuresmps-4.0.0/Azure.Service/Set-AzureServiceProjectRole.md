---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023910"
---
# <span data-ttu-id="e640a-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="e640a-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="e640a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e640a-102">SYNOPSIS</span></span>
<span data-ttu-id="e640a-103">Imposta il numero di istanze o la versione di runtime di un ruolo.</span><span class="sxs-lookup"><span data-stu-id="e640a-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="e640a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e640a-104">SYNTAX</span></span>

### <span data-ttu-id="e640a-105">Istanze</span><span class="sxs-lookup"><span data-stu-id="e640a-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e640a-106">Runtime</span><span class="sxs-lookup"><span data-stu-id="e640a-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e640a-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="e640a-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e640a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e640a-108">DESCRIPTION</span></span>
<span data-ttu-id="e640a-109">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e640a-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e640a-110">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e640a-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e640a-111">Il cmdlet **set-AzureServiceProjectRole** imposta il numero di istanze di ruolo per il ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e640a-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="e640a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e640a-112">EXAMPLES</span></span>

### <span data-ttu-id="e640a-113">Esempio 1: impostare le istanze per un ruolo Web</span><span class="sxs-lookup"><span data-stu-id="e640a-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="e640a-114">Imposta il numero di istanze per il ruolo Web denominato MyWebRole1 su 2.</span><span class="sxs-lookup"><span data-stu-id="e640a-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="e640a-115">Esempio 2: impostare le istanze per un ruolo di lavoro</span><span class="sxs-lookup"><span data-stu-id="e640a-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="e640a-116">Imposta il conteggio delle istanze del ruolo per il ruolo di lavoro denominato WorkerRole1 su 2.</span><span class="sxs-lookup"><span data-stu-id="e640a-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="e640a-117">Esempio 3: impostare la versione di runtime per un servizio ruolo</span><span class="sxs-lookup"><span data-stu-id="e640a-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="e640a-118">Imposta la versione di runtime node.exe per il ruolo MyRole1 in 0.6.20.</span><span class="sxs-lookup"><span data-stu-id="e640a-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="e640a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e640a-119">PARAMETERS</span></span>

### <span data-ttu-id="e640a-120">-Istanze</span><span class="sxs-lookup"><span data-stu-id="e640a-120">-Instances</span></span>
<span data-ttu-id="e640a-121">Specifica il numero di istanze di ruolo per il Web o il ruolo di lavoro specificato.</span><span class="sxs-lookup"><span data-stu-id="e640a-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e640a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e640a-122">-PassThru</span></span>
<span data-ttu-id="e640a-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e640a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e640a-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e640a-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e640a-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="e640a-125">-Profile</span></span>
<span data-ttu-id="e640a-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e640a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e640a-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e640a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e640a-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="e640a-128">-RoleName</span></span>
<span data-ttu-id="e640a-129">Specifica il nome del Web o del ruolo di lavoro da modificare.</span><span class="sxs-lookup"><span data-stu-id="e640a-129">Specifies the name of the web or worker role to be changed.</span></span>

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

### <span data-ttu-id="e640a-130">-Runtime</span><span class="sxs-lookup"><span data-stu-id="e640a-130">-Runtime</span></span>
<span data-ttu-id="e640a-131">Specifica il runtime da aggiungere al ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e640a-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e640a-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="e640a-132">-Version</span></span>
<span data-ttu-id="e640a-133">Specifica la versione del runtime da aggiungere al ruolo.</span><span class="sxs-lookup"><span data-stu-id="e640a-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e640a-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="e640a-134">-VMSize</span></span>
<span data-ttu-id="e640a-135">Specifica le dimensioni della macchina virtuale del ruolo.</span><span class="sxs-lookup"><span data-stu-id="e640a-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e640a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e640a-136">CommonParameters</span></span>
<span data-ttu-id="e640a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e640a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e640a-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e640a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e640a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e640a-139">INPUTS</span></span>

###  
<span data-ttu-id="e640a-140">Specifica le dimensioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e640a-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="e640a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e640a-141">OUTPUTS</span></span>

## <span data-ttu-id="e640a-142">Note</span><span class="sxs-lookup"><span data-stu-id="e640a-142">NOTES</span></span>

## <span data-ttu-id="e640a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e640a-143">RELATED LINKS</span></span>

[<span data-ttu-id="e640a-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="e640a-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


