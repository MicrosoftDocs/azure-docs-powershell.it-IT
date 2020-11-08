---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029637"
---
# <span data-ttu-id="eafda-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="eafda-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="eafda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eafda-102">SYNOPSIS</span></span>
<span data-ttu-id="eafda-103">Rimuove un oggetto di configurazione ACL da una configurazione di una macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="eafda-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="eafda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eafda-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eafda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eafda-105">DESCRIPTION</span></span>
<span data-ttu-id="eafda-106">Il cmdlet **Remove-AzureAclConfig** rimuove un oggetto di configurazione dell'elenco di controllo di Access (ACL) da una configurazione di una macchina virtuale Azure.</span><span class="sxs-lookup"><span data-stu-id="eafda-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="eafda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eafda-107">EXAMPLES</span></span>

### <span data-ttu-id="eafda-108">Esempio 1: rimuovere una configurazione ACL</span><span class="sxs-lookup"><span data-stu-id="eafda-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="eafda-109">Questo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="eafda-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="eafda-110">Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="eafda-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eafda-111">Questo cmdlet rimuove la configurazione ACL per l'endpoint denominato Web.</span><span class="sxs-lookup"><span data-stu-id="eafda-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="eafda-112">Il comando passa il risultato al cmdlet **Update-AzureVM** , che aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eafda-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="eafda-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eafda-113">PARAMETERS</span></span>

### <span data-ttu-id="eafda-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="eafda-114">-EndpointName</span></span>
<span data-ttu-id="eafda-115">Specifica il nome dell'endpoint da cui questo cmdlet rimuove la configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="eafda-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

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

### <span data-ttu-id="eafda-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eafda-116">-InformationAction</span></span>
<span data-ttu-id="eafda-117">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="eafda-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eafda-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eafda-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eafda-119">Continuare</span><span class="sxs-lookup"><span data-stu-id="eafda-119">Continue</span></span>
- <span data-ttu-id="eafda-120">Ignora</span><span class="sxs-lookup"><span data-stu-id="eafda-120">Ignore</span></span>
- <span data-ttu-id="eafda-121">Informarsi</span><span class="sxs-lookup"><span data-stu-id="eafda-121">Inquire</span></span>
- <span data-ttu-id="eafda-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eafda-122">SilentlyContinue</span></span>
- <span data-ttu-id="eafda-123">Stop</span><span class="sxs-lookup"><span data-stu-id="eafda-123">Stop</span></span>
- <span data-ttu-id="eafda-124">Sospensione</span><span class="sxs-lookup"><span data-stu-id="eafda-124">Suspend</span></span>

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

### <span data-ttu-id="eafda-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eafda-125">-InformationVariable</span></span>
<span data-ttu-id="eafda-126">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="eafda-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eafda-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="eafda-127">-Profile</span></span>
<span data-ttu-id="eafda-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eafda-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eafda-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="eafda-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eafda-130">-VM</span><span class="sxs-lookup"><span data-stu-id="eafda-130">-VM</span></span>
<span data-ttu-id="eafda-131">Specifica la macchina virtuale da cui questo cmdlet rimuove una configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="eafda-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="eafda-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafda-132">CommonParameters</span></span>
<span data-ttu-id="eafda-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafda-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafda-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafda-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafda-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eafda-135">INPUTS</span></span>

## <span data-ttu-id="eafda-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eafda-136">OUTPUTS</span></span>

## <span data-ttu-id="eafda-137">Note</span><span class="sxs-lookup"><span data-stu-id="eafda-137">NOTES</span></span>

## <span data-ttu-id="eafda-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eafda-138">RELATED LINKS</span></span>

[<span data-ttu-id="eafda-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="eafda-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="eafda-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eafda-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="eafda-141">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="eafda-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="eafda-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="eafda-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="eafda-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="eafda-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


