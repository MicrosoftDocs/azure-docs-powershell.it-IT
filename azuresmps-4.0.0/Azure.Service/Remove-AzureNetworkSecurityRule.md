---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 8CDB4C0A-A050-4F65-8CC0-1822D006D772
online version: ''
schema: 2.0.0
ms.openlocfilehash: eb0fe27a664badd5f32b941e80b2c8e2cba2d2a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023827"
---
# <span data-ttu-id="49ae1-101">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="49ae1-101">Remove-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="49ae1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="49ae1-103">Rimuove una regola di sicurezza di rete da un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="49ae1-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="49ae1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49ae1-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityRule -Name <String> [-Force] -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="49ae1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="49ae1-106">Il cmdlet **Remove-AzureNetworkSecurityRule** rimuove una regola di sicurezza di rete di Azure da un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="49ae1-106">The **Remove-AzureNetworkSecurityRule** cmdlet removes an Azure network security rule from a network security group.</span></span>

## <span data-ttu-id="49ae1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49ae1-107">EXAMPLES</span></span>

## <span data-ttu-id="49ae1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49ae1-108">PARAMETERS</span></span>

### <span data-ttu-id="49ae1-109">-Force</span><span class="sxs-lookup"><span data-stu-id="49ae1-109">-Force</span></span>
<span data-ttu-id="49ae1-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="49ae1-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49ae1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="49ae1-111">-Name</span></span>
<span data-ttu-id="49ae1-112">Specifica il nome della regola di sicurezza della rete rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ae1-112">Specifies the name for the network security rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ae1-113">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="49ae1-113">-NetworkSecurityGroup</span></span>
<span data-ttu-id="49ae1-114">Specifica il gruppo di sicurezza di rete modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ae1-114">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="49ae1-115">Per ottenere un oggetto **INetworkSecurityGroup** , usa il cmdlet Get-AzureNetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="49ae1-115">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ae1-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="49ae1-116">-Profile</span></span>
<span data-ttu-id="49ae1-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ae1-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="49ae1-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="49ae1-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="49ae1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ae1-119">CommonParameters</span></span>
<span data-ttu-id="49ae1-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ae1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ae1-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ae1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ae1-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49ae1-122">INPUTS</span></span>

## <span data-ttu-id="49ae1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49ae1-123">OUTPUTS</span></span>

## <span data-ttu-id="49ae1-124">Note</span><span class="sxs-lookup"><span data-stu-id="49ae1-124">NOTES</span></span>

## <span data-ttu-id="49ae1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49ae1-125">RELATED LINKS</span></span>

[<span data-ttu-id="49ae1-126">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="49ae1-126">Set-AzureNetworkSecurityRule</span></span>](./Set-AzureNetworkSecurityRule.md)


