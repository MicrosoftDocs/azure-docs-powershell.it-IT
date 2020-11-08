---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029477"
---
# <span data-ttu-id="5fced-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5fced-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="5fced-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fced-102">SYNOPSIS</span></span>
<span data-ttu-id="5fced-103">Aggiorna le proprietà di un'entità di protezione nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="5fced-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="5fced-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fced-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5fced-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fced-105">DESCRIPTION</span></span>
<span data-ttu-id="5fced-106">Il cmdlet **Update-AzureSiteRecoveryProtectionEntity** aggiorna le proprietà di un'entità di protezione nel ripristino del sito di Azure, ad esempio le informazioni sul proprietario della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5fced-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="5fced-107">Questo cmdlet è supportato solo per Virtual Machine Monitor (VMM) per le entità di protezione protette di VMM.</span><span class="sxs-lookup"><span data-stu-id="5fced-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="5fced-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fced-108">EXAMPLES</span></span>

### <span data-ttu-id="5fced-109">Esempio 1: aggiornare un'entità di protezione</span><span class="sxs-lookup"><span data-stu-id="5fced-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="5fced-110">Il primo comando ottiene un contenitore protetto usando il cmdlet **Get-AzureSiteRecoveryProtectionContainer** e quindi archivia tale oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="5fced-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="5fced-111">Il secondo comando ottiene la macchina virtuale protetta che appartiene al contenitore archiviato in $Container usando il cmdlet **Get-AzureSiteRecoveryProtectionEntity** e lo archivia nella variabile $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="5fced-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="5fced-112">Il comando finale aggiorna l'entità di protezione in $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="5fced-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="5fced-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fced-113">PARAMETERS</span></span>

### <span data-ttu-id="5fced-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="5fced-114">-Profile</span></span>
<span data-ttu-id="5fced-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fced-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5fced-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5fced-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5fced-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5fced-117">-ProtectionEntity</span></span>
<span data-ttu-id="5fced-118">Specifica un'entità di protezione da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5fced-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="5fced-119">Per ottenere un oggetto **ASRProtectionEntity** , usa il cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5fced-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fced-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5fced-120">-WaitForCompletion</span></span>
<span data-ttu-id="5fced-121">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5fced-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5fced-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fced-122">CommonParameters</span></span>
<span data-ttu-id="5fced-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fced-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fced-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fced-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fced-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fced-125">INPUTS</span></span>

## <span data-ttu-id="5fced-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fced-126">OUTPUTS</span></span>

## <span data-ttu-id="5fced-127">Note</span><span class="sxs-lookup"><span data-stu-id="5fced-127">NOTES</span></span>

## <span data-ttu-id="5fced-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fced-128">RELATED LINKS</span></span>

[<span data-ttu-id="5fced-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5fced-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5fced-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5fced-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="5fced-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5fced-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


