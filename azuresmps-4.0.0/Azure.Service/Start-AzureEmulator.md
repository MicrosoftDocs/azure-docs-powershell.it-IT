---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029493"
---
# <span data-ttu-id="7af3a-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="7af3a-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="7af3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7af3a-102">SYNOPSIS</span></span>
<span data-ttu-id="7af3a-103">Avvia gli emulatori COMPUTE e storage.</span><span class="sxs-lookup"><span data-stu-id="7af3a-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="7af3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7af3a-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7af3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7af3a-105">DESCRIPTION</span></span>
<span data-ttu-id="7af3a-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7af3a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7af3a-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7af3a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7af3a-108">Il cmdlet **Start-AzureEmulator** avvia sia gli emulatori Compute che storage e ospita il servizio corrente nell'emulatore di calcolo.</span><span class="sxs-lookup"><span data-stu-id="7af3a-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="7af3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7af3a-109">EXAMPLES</span></span>

### <span data-ttu-id="7af3a-110">Esempio 1: avviare l'emulatore e avviare un browser</span><span class="sxs-lookup"><span data-stu-id="7af3a-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="7af3a-111">In questo esempio viene eseguito il servizio nell'emulatore di Azure e viene avviata una nuova finestra del browser nel servizio emulato.</span><span class="sxs-lookup"><span data-stu-id="7af3a-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="7af3a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7af3a-112">PARAMETERS</span></span>

### <span data-ttu-id="7af3a-113">-Avvio</span><span class="sxs-lookup"><span data-stu-id="7af3a-113">-Launch</span></span>
<span data-ttu-id="7af3a-114">Apre una nuova finestra del browser nel servizio dopo averla ospitata nell'emulatore.</span><span class="sxs-lookup"><span data-stu-id="7af3a-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af3a-115">-Modalità</span><span class="sxs-lookup"><span data-stu-id="7af3a-115">-Mode</span></span>
<span data-ttu-id="7af3a-116">Specifica la modalità di emulazione.</span><span class="sxs-lookup"><span data-stu-id="7af3a-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="7af3a-117">I valori validi sono: Full ed Express.</span><span class="sxs-lookup"><span data-stu-id="7af3a-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="7af3a-118">Il valore predefinito è Express.</span><span class="sxs-lookup"><span data-stu-id="7af3a-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af3a-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="7af3a-119">-Profile</span></span>
<span data-ttu-id="7af3a-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7af3a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7af3a-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7af3a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7af3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af3a-122">CommonParameters</span></span>
<span data-ttu-id="7af3a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af3a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af3a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af3a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7af3a-125">INPUTS</span></span>

## <span data-ttu-id="7af3a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7af3a-126">OUTPUTS</span></span>

## <span data-ttu-id="7af3a-127">Note</span><span class="sxs-lookup"><span data-stu-id="7af3a-127">NOTES</span></span>

## <span data-ttu-id="7af3a-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7af3a-128">RELATED LINKS</span></span>

[<span data-ttu-id="7af3a-129">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7af3a-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="7af3a-130">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7af3a-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="7af3a-131">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="7af3a-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


