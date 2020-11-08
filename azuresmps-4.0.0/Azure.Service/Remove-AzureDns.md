---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029941"
---
# <span data-ttu-id="38c03-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="38c03-101">Remove-AzureDns</span></span>

## <span data-ttu-id="38c03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38c03-102">SYNOPSIS</span></span>
<span data-ttu-id="38c03-103">Rimuove un server DNS da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="38c03-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="38c03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38c03-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38c03-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38c03-105">DESCRIPTION</span></span>
<span data-ttu-id="38c03-106">Il cmdlet **Remove-AzureDns** rimuove un server DNS da un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="38c03-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="38c03-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38c03-107">EXAMPLES</span></span>

### <span data-ttu-id="38c03-108">Esempio 1: rimuovere un server DNS da un servizio</span><span class="sxs-lookup"><span data-stu-id="38c03-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="38c03-109">Questo comando rimuove il server DNS denominato Dns07 da ContosoService.</span><span class="sxs-lookup"><span data-stu-id="38c03-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="38c03-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38c03-110">PARAMETERS</span></span>

### <span data-ttu-id="38c03-111">-Force</span><span class="sxs-lookup"><span data-stu-id="38c03-111">-Force</span></span>
<span data-ttu-id="38c03-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="38c03-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c03-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38c03-113">-InformationAction</span></span>
<span data-ttu-id="38c03-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="38c03-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38c03-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="38c03-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38c03-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="38c03-116">Continue</span></span>
- <span data-ttu-id="38c03-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="38c03-117">Ignore</span></span>
- <span data-ttu-id="38c03-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="38c03-118">Inquire</span></span>
- <span data-ttu-id="38c03-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38c03-119">SilentlyContinue</span></span>
- <span data-ttu-id="38c03-120">Stop</span><span class="sxs-lookup"><span data-stu-id="38c03-120">Stop</span></span>
- <span data-ttu-id="38c03-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="38c03-121">Suspend</span></span>

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

### <span data-ttu-id="38c03-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38c03-122">-InformationVariable</span></span>
<span data-ttu-id="38c03-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="38c03-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38c03-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="38c03-124">-Name</span></span>
<span data-ttu-id="38c03-125">Specifica il nome del server DNS rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c03-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38c03-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="38c03-126">-Profile</span></span>
<span data-ttu-id="38c03-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c03-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38c03-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="38c03-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38c03-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="38c03-129">-ServiceName</span></span>
<span data-ttu-id="38c03-130">Specifica il nome del servizio da cui questo cmdlet rimuove un server DNS.</span><span class="sxs-lookup"><span data-stu-id="38c03-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="38c03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c03-131">CommonParameters</span></span>
<span data-ttu-id="38c03-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c03-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c03-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c03-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38c03-134">INPUTS</span></span>

## <span data-ttu-id="38c03-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38c03-135">OUTPUTS</span></span>

### <span data-ttu-id="38c03-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="38c03-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="38c03-137">Note</span><span class="sxs-lookup"><span data-stu-id="38c03-137">NOTES</span></span>

## <span data-ttu-id="38c03-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38c03-138">RELATED LINKS</span></span>

[<span data-ttu-id="38c03-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="38c03-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="38c03-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="38c03-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="38c03-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="38c03-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="38c03-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="38c03-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


