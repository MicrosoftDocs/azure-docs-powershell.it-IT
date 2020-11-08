---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8170AEF9-46E6-4087-8A68-29DFD5D014B5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb63d143ca2cafce92109e17fd3ced6a9dc070e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023782"
---
# <span data-ttu-id="67877-101">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="67877-101">Set-AzureRole</span></span>

## <span data-ttu-id="67877-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67877-102">SYNOPSIS</span></span>
<span data-ttu-id="67877-103">Imposta il numero di istanze di un ruolo di Azure da eseguire.</span><span class="sxs-lookup"><span data-stu-id="67877-103">Sets the number of instances of an Azure role to run.</span></span>

## <span data-ttu-id="67877-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67877-104">SYNTAX</span></span>

```
Set-AzureRole [-ServiceName] <String> [-Slot] <String> [-RoleName] <String> [-Count] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="67877-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67877-105">DESCRIPTION</span></span>
<span data-ttu-id="67877-106">Il cmdlet **set-AzureRole** imposta il numero di istanze di un ruolo specificato da eseguire in una distribuzione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67877-106">The **Set-AzureRole** cmdlet sets the number of instances of a specified role to run in an Azure deployment.</span></span>

## <span data-ttu-id="67877-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67877-107">EXAMPLES</span></span>

### <span data-ttu-id="67877-108">1: impostare il numero di istanze per un ruolo</span><span class="sxs-lookup"><span data-stu-id="67877-108">1: Set the number of instances for a role</span></span>
```
PS C:\> Set-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestRole03" -Count 3
```

<span data-ttu-id="67877-109">Questo comando imposta il ruolo MyTestRole03 che viene eseguito in produzione nel servizio MySvc01 per avere tre istanze.</span><span class="sxs-lookup"><span data-stu-id="67877-109">This command sets the MyTestRole03 role that is running in production on the MySvc01 service to have three instances.</span></span>

## <span data-ttu-id="67877-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67877-110">PARAMETERS</span></span>

### <span data-ttu-id="67877-111">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="67877-111">-Count</span></span>
<span data-ttu-id="67877-112">Specifica il numero di istanze di ruolo da eseguire.</span><span class="sxs-lookup"><span data-stu-id="67877-112">Specifies the number of role instances to run.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67877-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="67877-113">-InformationAction</span></span>
<span data-ttu-id="67877-114">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="67877-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="67877-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="67877-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67877-116">Continuare</span><span class="sxs-lookup"><span data-stu-id="67877-116">Continue</span></span>
- <span data-ttu-id="67877-117">Ignora</span><span class="sxs-lookup"><span data-stu-id="67877-117">Ignore</span></span>
- <span data-ttu-id="67877-118">Informarsi</span><span class="sxs-lookup"><span data-stu-id="67877-118">Inquire</span></span>
- <span data-ttu-id="67877-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="67877-119">SilentlyContinue</span></span>
- <span data-ttu-id="67877-120">Stop</span><span class="sxs-lookup"><span data-stu-id="67877-120">Stop</span></span>
- <span data-ttu-id="67877-121">Sospensione</span><span class="sxs-lookup"><span data-stu-id="67877-121">Suspend</span></span>

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

### <span data-ttu-id="67877-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="67877-122">-InformationVariable</span></span>
<span data-ttu-id="67877-123">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="67877-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="67877-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="67877-124">-Profile</span></span>
<span data-ttu-id="67877-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67877-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67877-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="67877-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67877-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="67877-127">-RoleName</span></span>
<span data-ttu-id="67877-128">Specifica il nome del ruolo per cui impostare il numero di istanze.</span><span class="sxs-lookup"><span data-stu-id="67877-128">Specifies the name of the role for which to set the number of instances.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67877-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="67877-129">-ServiceName</span></span>
<span data-ttu-id="67877-130">Specifica il nome del servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="67877-130">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="67877-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="67877-131">-Slot</span></span>
<span data-ttu-id="67877-132">Specifica l'ambiente di distribuzione della distribuzione da modificare.</span><span class="sxs-lookup"><span data-stu-id="67877-132">Specifies the deployment environment of the deployment to modify.</span></span>
<span data-ttu-id="67877-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="67877-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67877-134">Produzione</span><span class="sxs-lookup"><span data-stu-id="67877-134">Production</span></span>
- <span data-ttu-id="67877-135">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="67877-135">Staging</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67877-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67877-136">CommonParameters</span></span>
<span data-ttu-id="67877-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67877-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67877-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67877-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67877-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67877-139">INPUTS</span></span>

## <span data-ttu-id="67877-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67877-140">OUTPUTS</span></span>

## <span data-ttu-id="67877-141">Note</span><span class="sxs-lookup"><span data-stu-id="67877-141">NOTES</span></span>

## <span data-ttu-id="67877-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67877-142">RELATED LINKS</span></span>

[<span data-ttu-id="67877-143">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="67877-143">Get-AzureRole</span></span>](./Get-AzureRole.md)


