---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029634"
---
# <span data-ttu-id="7d5bf-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7d5bf-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="7d5bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d5bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5bf-103">Elimina un gruppo di affinità in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="7d5bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d5bf-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d5bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d5bf-105">DESCRIPTION</span></span>
<span data-ttu-id="7d5bf-106">Il cmdlet **Remove-AzureAffinityGroup** Elimina un gruppo di affinità di Azure nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="7d5bf-107">Non è possibile eliminare un gruppo di affinità che include membri.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="7d5bf-108">È prima di tutto necessario eliminare tutti i membri di un gruppo di affinità.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="7d5bf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d5bf-109">EXAMPLES</span></span>

### <span data-ttu-id="7d5bf-110">Esempio 1: rimuovere un gruppo di affinità</span><span class="sxs-lookup"><span data-stu-id="7d5bf-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="7d5bf-111">Questo comando Elimina il gruppo di affinità South01 nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="7d5bf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d5bf-112">PARAMETERS</span></span>

### <span data-ttu-id="7d5bf-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7d5bf-113">-InformationAction</span></span>
<span data-ttu-id="7d5bf-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7d5bf-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d5bf-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7d5bf-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="7d5bf-116">Continue</span></span>
- <span data-ttu-id="7d5bf-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="7d5bf-117">Ignore</span></span>
- <span data-ttu-id="7d5bf-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7d5bf-118">Inquire</span></span>
- <span data-ttu-id="7d5bf-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7d5bf-119">SilentlyContinue</span></span>
- <span data-ttu-id="7d5bf-120">Stop</span><span class="sxs-lookup"><span data-stu-id="7d5bf-120">Stop</span></span>
- <span data-ttu-id="7d5bf-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7d5bf-121">Suspend</span></span>

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

### <span data-ttu-id="7d5bf-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7d5bf-122">-InformationVariable</span></span>
<span data-ttu-id="7d5bf-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7d5bf-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d5bf-124">-Name</span></span>
<span data-ttu-id="7d5bf-125">Specifica il nome del gruppo di affinità eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="7d5bf-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="7d5bf-126">-Profile</span></span>
<span data-ttu-id="7d5bf-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d5bf-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d5bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5bf-129">CommonParameters</span></span>
<span data-ttu-id="7d5bf-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d5bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5bf-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d5bf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5bf-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d5bf-132">INPUTS</span></span>

## <span data-ttu-id="7d5bf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d5bf-133">OUTPUTS</span></span>

## <span data-ttu-id="7d5bf-134">Note</span><span class="sxs-lookup"><span data-stu-id="7d5bf-134">NOTES</span></span>

## <span data-ttu-id="7d5bf-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d5bf-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d5bf-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7d5bf-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="7d5bf-137">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7d5bf-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="7d5bf-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="7d5bf-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


