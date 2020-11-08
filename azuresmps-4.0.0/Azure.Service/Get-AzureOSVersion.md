---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023595"
---
# <span data-ttu-id="a34f1-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="a34f1-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="a34f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a34f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a34f1-103">Elenca tutti i sistemi operativi di Azure Guest.</span><span class="sxs-lookup"><span data-stu-id="a34f1-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="a34f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a34f1-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a34f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a34f1-105">DESCRIPTION</span></span>
<span data-ttu-id="a34f1-106">Il cmdlet **Get-AzureOSVersion** elenca tutti i sistemi operativi di Azure Guest disponibili.</span><span class="sxs-lookup"><span data-stu-id="a34f1-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="a34f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a34f1-107">EXAMPLES</span></span>

### <span data-ttu-id="a34f1-108">Esempio 1: ottenere tutti i sistemi operativi disponibili</span><span class="sxs-lookup"><span data-stu-id="a34f1-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="a34f1-109">Questo comando Recupera un oggetto che contiene un elenco di tutte le versioni dei sistemi operativi guest disponibili nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a34f1-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="a34f1-110">Esempio 2: visualizzare le informazioni sul sistema operativo in una tabella</span><span class="sxs-lookup"><span data-stu-id="a34f1-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="a34f1-111">Questo comando Recupera un oggetto che contiene un elenco di tutte le versioni dei sistemi operativi guest disponibili nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a34f1-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="a34f1-112">Il comando li passa al cmdlet **Format-Table** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="a34f1-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a34f1-113">Questo cmdlet li formatta come tabella che mostra la famiglia di sistemi operativi, l'etichetta della famiglia di sistemi operativi e la versione.</span><span class="sxs-lookup"><span data-stu-id="a34f1-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="a34f1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a34f1-114">PARAMETERS</span></span>

### <span data-ttu-id="a34f1-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a34f1-115">-InformationAction</span></span>
<span data-ttu-id="a34f1-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="a34f1-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a34f1-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a34f1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a34f1-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="a34f1-118">Continue</span></span>
- <span data-ttu-id="a34f1-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="a34f1-119">Ignore</span></span>
- <span data-ttu-id="a34f1-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="a34f1-120">Inquire</span></span>
- <span data-ttu-id="a34f1-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a34f1-121">SilentlyContinue</span></span>
- <span data-ttu-id="a34f1-122">Stop</span><span class="sxs-lookup"><span data-stu-id="a34f1-122">Stop</span></span>
- <span data-ttu-id="a34f1-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="a34f1-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34f1-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a34f1-124">-InformationVariable</span></span>
<span data-ttu-id="a34f1-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="a34f1-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a34f1-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="a34f1-126">-Profile</span></span>
<span data-ttu-id="a34f1-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a34f1-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a34f1-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a34f1-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a34f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a34f1-129">CommonParameters</span></span>
<span data-ttu-id="a34f1-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a34f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a34f1-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a34f1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a34f1-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a34f1-132">INPUTS</span></span>

## <span data-ttu-id="a34f1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a34f1-133">OUTPUTS</span></span>

## <span data-ttu-id="a34f1-134">Note</span><span class="sxs-lookup"><span data-stu-id="a34f1-134">NOTES</span></span>

## <span data-ttu-id="a34f1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a34f1-135">RELATED LINKS</span></span>

[<span data-ttu-id="a34f1-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="a34f1-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


