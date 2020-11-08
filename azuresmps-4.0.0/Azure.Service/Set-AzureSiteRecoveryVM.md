---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 30D56D40-2EA0-48D1-846A-AFB4A987E08F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9dac9858a251e0390fd2a11a2c01dddede1613b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023712"
---
# <span data-ttu-id="6769b-101">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="6769b-101">Set-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="6769b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6769b-102">SYNOPSIS</span></span>
<span data-ttu-id="6769b-103">Imposta le opzioni sul lato ripristino per un'entità di protezione del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="6769b-103">Sets the recovery-side options for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="6769b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6769b-104">SYNTAX</span></span>

```
Set-AzureSiteRecoveryVM -VirtualMachine <ASRVirtualMachine> [-Name <String>] [-Size <String>]
 [-PrimaryNic <String>] [-RecoveryNetworkId <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6769b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6769b-105">DESCRIPTION</span></span>
<span data-ttu-id="6769b-106">Il cmdlet **set-AzureSiteRecoveryVM** imposta le opzioni di protezione sul lato del ripristino, ad esempio la dimensione della macchina virtuale di ripristino e la rete Virtual Machine di ripristino, per le entità di protezione del ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="6769b-106">The **Set-AzureSiteRecoveryVM** cmdlet sets the recovery-side protection options, such as the recovery virtual machine size and recovery virtual machine network, for Azure Site Recovery protection entities.</span></span>

## <span data-ttu-id="6769b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6769b-107">EXAMPLES</span></span>

### <span data-ttu-id="6769b-108">Esempio 1: consentire l'aggiornamento in una macchina virtuale protetta</span><span class="sxs-lookup"><span data-stu-id="6769b-108">Example 1: Allow the update on a protected virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $VirtualMachines = Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer 
PS C:\> Set-AzureSiteRecoveryVM -VirtualMachine $VirtualMachines[0] -Name "NewVirtualMachine05"
Name             : 
ID               : 8170d274-1e48-404a-b080-172ada140bc3
ClientRequestId  : 09354052-8430-4fa8-9a35-63196dd4b2b4-2015-02-03 04:19:06Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="6769b-109">Il primo comando usa il cmdlet **Get-AzureSiteRecoveryProtectionContainer** per ottenere un contenitore protetto e lo archivia nella variabile $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="6769b-109">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="6769b-110">Il secondo comando recupera le macchine virtuali in $ProtectionContainer, usando il cmdlet **Get-AzureSiteRecoveryVM** e quindi le archivia nella variabile $VitrualMachines.</span><span class="sxs-lookup"><span data-stu-id="6769b-110">The second command gets the virtual machines in $ProtectionContainer, by using the **Get-AzureSiteRecoveryVM** cmdlet, and then stores them in the $VitrualMachines variable.</span></span>

<span data-ttu-id="6769b-111">Il comando finale consente gli aggiornamenti per la prima macchina virtuale nella matrice $VitrualMachines, denominata NewVirtualMachine05.</span><span class="sxs-lookup"><span data-stu-id="6769b-111">The final command allows updates for the first virtual machine in the $VitrualMachines array, named NewVirtualMachine05.</span></span>

## <span data-ttu-id="6769b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6769b-112">PARAMETERS</span></span>

### <span data-ttu-id="6769b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6769b-113">-Name</span></span>
<span data-ttu-id="6769b-114">Specifica il nome della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6769b-114">Specifies the name of the target virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6769b-115">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="6769b-115">-PrimaryNic</span></span>
<span data-ttu-id="6769b-116">Specifica la scheda di rete principale.</span><span class="sxs-lookup"><span data-stu-id="6769b-116">Specifies the primary network adapter card.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6769b-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="6769b-117">-Profile</span></span>
<span data-ttu-id="6769b-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6769b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6769b-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6769b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6769b-120">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="6769b-120">-RecoveryNetworkId</span></span>
<span data-ttu-id="6769b-121">Specifica l'ID della rete di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6769b-121">Specifies the recovery network ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6769b-122">-Dimensione</span><span class="sxs-lookup"><span data-stu-id="6769b-122">-Size</span></span>
<span data-ttu-id="6769b-123">Specifica la dimensione della macchina virtuale di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6769b-123">Specifies the target virtual machine size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6769b-124">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6769b-124">-VirtualMachine</span></span>
<span data-ttu-id="6769b-125">Specifica l'oggetto macchina virtuale ripristino sito.</span><span class="sxs-lookup"><span data-stu-id="6769b-125">Specifies the Site Recovery virtual machine object.</span></span>

```yaml
Type: ASRVirtualMachine
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6769b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6769b-126">CommonParameters</span></span>
<span data-ttu-id="6769b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6769b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6769b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6769b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6769b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6769b-129">INPUTS</span></span>

## <span data-ttu-id="6769b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6769b-130">OUTPUTS</span></span>

## <span data-ttu-id="6769b-131">Note</span><span class="sxs-lookup"><span data-stu-id="6769b-131">NOTES</span></span>

## <span data-ttu-id="6769b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6769b-132">RELATED LINKS</span></span>

[<span data-ttu-id="6769b-133">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6769b-133">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="6769b-134">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="6769b-134">Get-AzureSiteRecoveryVM</span></span>](./Get-AzureSiteRecoveryVM.md)


