---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029967"
---
# <span data-ttu-id="c8218-101">Get-AzureWinRMUri</span><span class="sxs-lookup"><span data-stu-id="c8218-101">Get-AzureWinRMUri</span></span>

## <span data-ttu-id="c8218-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8218-102">SYNOPSIS</span></span>
<span data-ttu-id="c8218-103">Ottiene l'URI per il listener HTTPS di WinRM in una macchina virtuale o un elenco di macchine virtuali in un servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="c8218-103">Gets the URI to WinRM https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="c8218-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8218-104">SYNTAX</span></span>

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c8218-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8218-105">DESCRIPTION</span></span>
<span data-ttu-id="c8218-106">Il cmdlet **Get-AzureWinRMUri** Ottiene l'URI del listener HTTPS di gestione remota di Windows (WinRM) in una macchina virtuale o un elenco di macchine virtuali in un servizio ospitato.</span><span class="sxs-lookup"><span data-stu-id="c8218-106">The **Get-AzureWinRMUri** cmdlet gets the URI of the Windows Remote Management (WinRM) https listener to a virtual machine or a list of virtual machines in a hosted service.</span></span>

## <span data-ttu-id="c8218-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8218-107">EXAMPLES</span></span>

### <span data-ttu-id="c8218-108">Esempio 1: ottenere l'URI del listener HTTPS di WinRM in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="c8218-108">Example 1: Get the URI of the WinRM https listener to a virtual machine</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

<span data-ttu-id="c8218-109">Questo comando consente di ottenere la UIR del listener HTTPS di WinRM in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8218-109">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

### <span data-ttu-id="c8218-110">Esempio 2: ottenere l'URI del listener HTTPS di WinRM in una macchina virtuale di un servizio specifico</span><span class="sxs-lookup"><span data-stu-id="c8218-110">Example 2: Get the URI of the WinRM https listener to a virtual machine of a specific service</span></span>
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

<span data-ttu-id="c8218-111">Questo comando consente di ottenere la UIR del listener HTTPS di WinRM in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8218-111">This command gets the UIR of the WinRM https listener to a virtual machine.</span></span>

## <span data-ttu-id="c8218-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8218-112">PARAMETERS</span></span>

### <span data-ttu-id="c8218-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c8218-113">-InformationAction</span></span>
<span data-ttu-id="c8218-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="c8218-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c8218-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8218-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8218-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="c8218-116">Continue</span></span>
- <span data-ttu-id="c8218-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="c8218-117">Ignore</span></span>
- <span data-ttu-id="c8218-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="c8218-118">Inquire</span></span>
- <span data-ttu-id="c8218-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c8218-119">SilentlyContinue</span></span>
- <span data-ttu-id="c8218-120">Stop</span><span class="sxs-lookup"><span data-stu-id="c8218-120">Stop</span></span>
- <span data-ttu-id="c8218-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="c8218-121">Suspend</span></span>

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

### <span data-ttu-id="c8218-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c8218-122">-InformationVariable</span></span>
<span data-ttu-id="c8218-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="c8218-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c8218-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8218-124">-Name</span></span>
<span data-ttu-id="c8218-125">Specifica il nome della macchina virtuale a cui viene generato l'URI di WinRM.</span><span class="sxs-lookup"><span data-stu-id="c8218-125">Specifies the name of the virtual machine to which the WinRM URI is generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8218-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="c8218-126">-Profile</span></span>
<span data-ttu-id="c8218-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8218-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8218-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c8218-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8218-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c8218-129">-ServiceName</span></span>
<span data-ttu-id="c8218-130">Specifica il nome del servizio Microsoft Azure che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c8218-130">Specifies the name of the Microsoft Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8218-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8218-131">CommonParameters</span></span>
<span data-ttu-id="c8218-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8218-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8218-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8218-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8218-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8218-134">INPUTS</span></span>

## <span data-ttu-id="c8218-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8218-135">OUTPUTS</span></span>

## <span data-ttu-id="c8218-136">Note</span><span class="sxs-lookup"><span data-stu-id="c8218-136">NOTES</span></span>

## <span data-ttu-id="c8218-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8218-137">RELATED LINKS</span></span>

[<span data-ttu-id="c8218-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c8218-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="c8218-139">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="c8218-139">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


