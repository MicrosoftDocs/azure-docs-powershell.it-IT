---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023631"
---
# <span data-ttu-id="0fdba-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0fdba-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="0fdba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fdba-102">SYNOPSIS</span></span>
<span data-ttu-id="0fdba-103">Ottiene l'oggetto di configurazione ACL da una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fdba-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="0fdba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fdba-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0fdba-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fdba-105">DESCRIPTION</span></span>
<span data-ttu-id="0fdba-106">Il cmdlet **Get-AzureAclConfig** Ottiene l'oggetto di configurazione dell'elenco di controllo di accesso (ACL) da una macchina virtuale di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="0fdba-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="0fdba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fdba-107">EXAMPLES</span></span>

### <span data-ttu-id="0fdba-108">Esempio 1: ottenere un oggetto di configurazione ACL per un endpoint di una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0fdba-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="0fdba-109">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="0fdba-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="0fdba-110">Il comando passa l'oggetto al cmdlet **Get-AzureAclConfig** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="0fdba-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0fdba-111">Questo cmdlet ottiene la configurazione ACL per l'endpoint denominato Web.</span><span class="sxs-lookup"><span data-stu-id="0fdba-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="0fdba-112">Il comando Archivia l'oggetto di configurazione ACL nella variabile $Acl.</span><span class="sxs-lookup"><span data-stu-id="0fdba-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="0fdba-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fdba-113">PARAMETERS</span></span>

### <span data-ttu-id="0fdba-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0fdba-114">-EndpointName</span></span>
<span data-ttu-id="0fdba-115">Specifica il nome dell'endpoint per cui questo cmdlet ottiene un ACL.</span><span class="sxs-lookup"><span data-stu-id="0fdba-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fdba-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0fdba-116">-InformationAction</span></span>
<span data-ttu-id="0fdba-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="0fdba-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0fdba-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0fdba-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0fdba-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="0fdba-119">Continue</span></span>
- <span data-ttu-id="0fdba-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="0fdba-120">Ignore</span></span>
- <span data-ttu-id="0fdba-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="0fdba-121">Inquire</span></span>
- <span data-ttu-id="0fdba-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0fdba-122">SilentlyContinue</span></span>
- <span data-ttu-id="0fdba-123">Stop</span><span class="sxs-lookup"><span data-stu-id="0fdba-123">Stop</span></span>
- <span data-ttu-id="0fdba-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="0fdba-124">Suspend</span></span>

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

### <span data-ttu-id="0fdba-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0fdba-125">-InformationVariable</span></span>
<span data-ttu-id="0fdba-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="0fdba-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0fdba-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="0fdba-127">-Profile</span></span>
<span data-ttu-id="0fdba-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fdba-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0fdba-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0fdba-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0fdba-130">-VM</span><span class="sxs-lookup"><span data-stu-id="0fdba-130">-VM</span></span>
<span data-ttu-id="0fdba-131">Specifica l'oggetto macchina virtuale per cui questo cmdlet ottiene la configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="0fdba-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fdba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fdba-132">CommonParameters</span></span>
<span data-ttu-id="0fdba-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fdba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fdba-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fdba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fdba-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fdba-135">INPUTS</span></span>

## <span data-ttu-id="0fdba-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fdba-136">OUTPUTS</span></span>

## <span data-ttu-id="0fdba-137">Note</span><span class="sxs-lookup"><span data-stu-id="0fdba-137">NOTES</span></span>

## <span data-ttu-id="0fdba-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fdba-138">RELATED LINKS</span></span>

[<span data-ttu-id="0fdba-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="0fdba-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="0fdba-140">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0fdba-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="0fdba-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0fdba-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="0fdba-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="0fdba-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


