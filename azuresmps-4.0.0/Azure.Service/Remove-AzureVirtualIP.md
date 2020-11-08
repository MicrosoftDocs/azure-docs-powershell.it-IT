---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023445"
---
# <span data-ttu-id="9d9ae-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="9d9ae-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="9d9ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d9ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9ae-103">Elimina un indirizzo IP virtuale dal servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="9d9ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d9ae-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9d9ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d9ae-105">DESCRIPTION</span></span>
<span data-ttu-id="9d9ae-106">Il cmdlet **Remove-AzureVirtualIP** Elimina un IP virtuale (VIP) da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="9d9ae-107">L'operazione viene eseguita correttamente solo se nell'IP virtuale non sono associati endpoint.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="9d9ae-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d9ae-108">EXAMPLES</span></span>

### <span data-ttu-id="9d9ae-109">Esempio 1: rimuovere un indirizzo IP virtuale da un servizio</span><span class="sxs-lookup"><span data-stu-id="9d9ae-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="9d9ae-110">Questo comando rimuove un indirizzo IP virtuale da un servizio.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="9d9ae-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d9ae-111">PARAMETERS</span></span>

### <span data-ttu-id="9d9ae-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9d9ae-112">-Force</span></span>
<span data-ttu-id="9d9ae-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d9ae-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9d9ae-114">-InformationAction</span></span>
<span data-ttu-id="9d9ae-115">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d9ae-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9d9ae-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d9ae-117">Continuare</span><span class="sxs-lookup"><span data-stu-id="9d9ae-117">Continue</span></span>
- <span data-ttu-id="9d9ae-118">Ignora</span><span class="sxs-lookup"><span data-stu-id="9d9ae-118">Ignore</span></span>
- <span data-ttu-id="9d9ae-119">Informarsi</span><span class="sxs-lookup"><span data-stu-id="9d9ae-119">Inquire</span></span>
- <span data-ttu-id="9d9ae-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d9ae-120">SilentlyContinue</span></span>
- <span data-ttu-id="9d9ae-121">Stop</span><span class="sxs-lookup"><span data-stu-id="9d9ae-121">Stop</span></span>
- <span data-ttu-id="9d9ae-122">Sospensione</span><span class="sxs-lookup"><span data-stu-id="9d9ae-122">Suspend</span></span>

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

### <span data-ttu-id="9d9ae-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d9ae-123">-InformationVariable</span></span>
<span data-ttu-id="9d9ae-124">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9d9ae-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="9d9ae-125">-Profile</span></span>
<span data-ttu-id="9d9ae-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d9ae-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d9ae-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9d9ae-128">-ServiceName</span></span>
<span data-ttu-id="9d9ae-129">Specifica il nome del servizio da cui rimuovere un indirizzo IP virtuale.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9ae-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="9d9ae-130">-VirtualIPName</span></span>
<span data-ttu-id="9d9ae-131">Specifica il nome dell'indirizzo IP virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-131">Specifies the name of the virtual IP address to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d9ae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9ae-132">CommonParameters</span></span>
<span data-ttu-id="9d9ae-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d9ae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9ae-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9ae-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9ae-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d9ae-135">INPUTS</span></span>

## <span data-ttu-id="9d9ae-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d9ae-136">OUTPUTS</span></span>

### <span data-ttu-id="9d9ae-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="9d9ae-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="9d9ae-138">Note</span><span class="sxs-lookup"><span data-stu-id="9d9ae-138">NOTES</span></span>

## <span data-ttu-id="9d9ae-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d9ae-139">RELATED LINKS</span></span>

[<span data-ttu-id="9d9ae-140">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="9d9ae-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


