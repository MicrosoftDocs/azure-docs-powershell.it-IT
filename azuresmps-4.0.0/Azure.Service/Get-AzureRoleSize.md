---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023573"
---
# <span data-ttu-id="9393c-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="9393c-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="9393c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9393c-102">SYNOPSIS</span></span>
<span data-ttu-id="9393c-103">Ottiene le informazioni sulle dimensioni del ruolo per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9393c-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="9393c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9393c-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9393c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9393c-105">DESCRIPTION</span></span>
<span data-ttu-id="9393c-106">Il cmdlet **Get-AzureRoleSize** ottiene le informazioni sulle dimensioni del ruolo per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9393c-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="9393c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9393c-107">EXAMPLES</span></span>

### <span data-ttu-id="9393c-108">Esempio 1: ottenere informazioni sulle dimensioni del ruolo</span><span class="sxs-lookup"><span data-stu-id="9393c-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="9393c-109">Questo comando ottiene le informazioni sulle dimensioni del ruolo per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9393c-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="9393c-110">Esempio 2: ottenere informazioni sulle dimensioni del ruolo e specificare il nome della dimensione del ruolo</span><span class="sxs-lookup"><span data-stu-id="9393c-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="9393c-111">Questo comando ottiene le informazioni sulle dimensioni del ruolo per le dimensioni del ruolo specificate.</span><span class="sxs-lookup"><span data-stu-id="9393c-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="9393c-112">Esempio 3: ottenere informazioni sulle dimensioni dei ruoli per tutte le macchine virtuali in tutti i servizi di Azure</span><span class="sxs-lookup"><span data-stu-id="9393c-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="9393c-113">Questo comando ottiene le informazioni sulle dimensioni dei ruoli per tutte le macchine virtuali in tutti i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="9393c-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="9393c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9393c-114">PARAMETERS</span></span>

### <span data-ttu-id="9393c-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9393c-115">-InformationAction</span></span>
<span data-ttu-id="9393c-116">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="9393c-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9393c-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9393c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9393c-118">Continuare</span><span class="sxs-lookup"><span data-stu-id="9393c-118">Continue</span></span>
- <span data-ttu-id="9393c-119">Ignora</span><span class="sxs-lookup"><span data-stu-id="9393c-119">Ignore</span></span>
- <span data-ttu-id="9393c-120">Informarsi</span><span class="sxs-lookup"><span data-stu-id="9393c-120">Inquire</span></span>
- <span data-ttu-id="9393c-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9393c-121">SilentlyContinue</span></span>
- <span data-ttu-id="9393c-122">Stop</span><span class="sxs-lookup"><span data-stu-id="9393c-122">Stop</span></span>
- <span data-ttu-id="9393c-123">Sospensione</span><span class="sxs-lookup"><span data-stu-id="9393c-123">Suspend</span></span>

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

### <span data-ttu-id="9393c-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9393c-124">-InformationVariable</span></span>
<span data-ttu-id="9393c-125">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="9393c-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9393c-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="9393c-126">-InstanceSize</span></span>
<span data-ttu-id="9393c-127">Specifica il nome della dimensione del ruolo, ad esempio: piccolissimo, piccolo, grande, esteso, a5, A6, a7.</span><span class="sxs-lookup"><span data-stu-id="9393c-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9393c-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="9393c-128">-Profile</span></span>
<span data-ttu-id="9393c-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9393c-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9393c-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="9393c-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9393c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9393c-131">CommonParameters</span></span>
<span data-ttu-id="9393c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9393c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9393c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9393c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9393c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9393c-134">INPUTS</span></span>

## <span data-ttu-id="9393c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9393c-135">OUTPUTS</span></span>

## <span data-ttu-id="9393c-136">Note</span><span class="sxs-lookup"><span data-stu-id="9393c-136">NOTES</span></span>

## <span data-ttu-id="9393c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9393c-137">RELATED LINKS</span></span>

[<span data-ttu-id="9393c-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="9393c-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="9393c-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="9393c-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="9393c-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9393c-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


