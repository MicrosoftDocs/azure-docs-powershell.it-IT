---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 1836F342-A05C-4402-95F7-833E50A1AB97
online version: ''
schema: 2.0.0
ms.openlocfilehash: c33d48755b731c27f12742e7c21efe39994bc751
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029616"
---
# <span data-ttu-id="2c9a3-101">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2c9a3-101">Remove-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="2c9a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9a3-103">Elimina un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-103">Deletes a network security group.</span></span>

## <span data-ttu-id="2c9a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c9a3-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroup -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c9a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c9a3-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9a3-106">Il cmdlet **Remove-AzureNetworkSecurityGroup** Elimina un gruppo di sicurezza di rete di Azure dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-106">The **Remove-AzureNetworkSecurityGroup** cmdlet deletes an Azure network security group from your subscription.</span></span>

## <span data-ttu-id="2c9a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c9a3-107">EXAMPLES</span></span>

## <span data-ttu-id="2c9a3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c9a3-108">PARAMETERS</span></span>

### <span data-ttu-id="2c9a3-109">-Force</span><span class="sxs-lookup"><span data-stu-id="2c9a3-109">-Force</span></span>
<span data-ttu-id="2c9a3-110">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c9a3-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c9a3-111">-Name</span></span>
<span data-ttu-id="2c9a3-112">Specifica il nome del gruppo di sicurezza di rete eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-112">Specifies the name of the network security group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2c9a3-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c9a3-113">-PassThru</span></span>
<span data-ttu-id="2c9a3-114">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2c9a3-115">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c9a3-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="2c9a3-116">-Profile</span></span>
<span data-ttu-id="2c9a3-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2c9a3-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2c9a3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9a3-119">CommonParameters</span></span>
<span data-ttu-id="2c9a3-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c9a3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c9a3-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9a3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9a3-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c9a3-122">INPUTS</span></span>

## <span data-ttu-id="2c9a3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c9a3-123">OUTPUTS</span></span>

## <span data-ttu-id="2c9a3-124">Note</span><span class="sxs-lookup"><span data-stu-id="2c9a3-124">NOTES</span></span>

## <span data-ttu-id="2c9a3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c9a3-125">RELATED LINKS</span></span>

[<span data-ttu-id="2c9a3-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2c9a3-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="2c9a3-127">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2c9a3-127">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)


